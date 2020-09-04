<template>
  <div class="mt-12">
      
    <b-form @submit.prevent="onSubmit" @reset="onReset" v-if="show" method="post">
      
      <h1>Contact me</h1>
      
    <b-form-group id="input-group-1"
        label="Name:"
        label-for="input-1"
        description="You can enter a company name."
    >
      <b-form-input
          id="input-1"
          v-model="form.from_name"
          required
        ></b-form-input>
    </b-form-group>

    <b-form-group
        id="input-group-2"
        label="Email:"
        label-for="input-2"
    >
        <b-form-input
          id="input-2"
          v-model="form.from_email"
          required
        ></b-form-input>
    </b-form-group>
    
    <b-form-group
    id="input-group-3"
    label="Reason for cantact?"
    label-for="input-3"
    >
      <b-form-textarea
      id="input-3"
      v-model="form.message"
      rows="3"
      max-rows="6"
      required>
      </b-form-textarea>
    </b-form-group>

      <div class="buttons">
      <b-button type="submit" pill variant="primary" class="btn-submit" value="Send">Submit</b-button>
      <b-button type="reset" pill variant="success" class="btn-reset">Reset</b-button>
      </div>
    </b-form>
  </div>
</template>

<script>
import { validationMixin } from 'vuelidate'
import { required } from 'vuelidate/lib/validators'
import emailjs from 'emailjs-com'

export default {
    data() {
      return {
        form: {
          from_email: '',
          from_name: '',
          message: ''
        },
        show: true
      }
    },
    mixins: [ validationMixin],
    validations: {
          from_email: { required },
          from_name: { required },
          message: { required }
    },
    created(){
          emailjs.init("user_mzSdREtAZxo1GMhyjSqrb")
    },
    methods: {
      onSubmit() {
        if (this.$validations === true){
          window.emailjs.sendForm('default_service', 'portfolio_template', this.form.from_email, this.form.from_name, this.form.message).then((result) =>
          {
            console.log('SENT FORM', result.status, result.text);
          }, (error) => {
            console.log('SENDING FORM FAILED', error);
          });
      }
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.from_email = ''
        this.form.from_name = ''
        this.form.message = ''
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }

</script>
<style scoped>
h1 {
    margin: 10% 0 10% 0;
}
.mt-12{
margin-left: 15%;
margin-top: 3vh;
width: 30%;

}

.buttons {
    margin-top: 10%;
}
.btn-submit {
    margin-right: 10px;
}
</style>