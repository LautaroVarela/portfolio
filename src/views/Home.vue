<template>
<div id="home">

    

    <b-container class="mt-12">
        <div class="cover">
            <b-img :src="require('@/assets/img/bg.jpg')"></b-img>
    </div>
        <b-row>
            <b-col cols="12">
        <h1 >Lautaro Varela´s portfolio.</h1>
        <p>In this site i will show you my profile, what it looks my career
        and what i love to do.</p>
    <div class="buttons">
        <b-button pill class="btn-projects" size="lg" variant="success" :to="{ name: 'projects' }">See my work</b-button>
        <b-button pill class="btn-linkedin" size="lg" variant="outline-success" @click="myLinkedin()"><i class="fab fa-linkedin-in"></i></b-button>
    </div>
            </b-col>
            
        </b-row>
            
        <!-- 
        <transition name="more" mode="out-in">
        <b-button @click="show = !show"><b-icon class="more" icon="chevron-down"></b-icon><b-icon class="less" icon="chevron-up"></b-icon></b-button>
        </transition>
        <transition name="info">
            <p v-if="show">I´m a JR frontend developer...</p>
        </transition>
        
    -->
    

    
    </b-container>
    






    
    

</div>
</template>

<script>

export default {
    data() {

        return {
         show: false,
         myModel: false
        }

    },
    
    methods: {
        myLinkedin() {
            window.open("https://www.linkedin.com/in/lautaro-varela/", "_blank")
                     }
            }



}
</script>
<style lang="scss" scoped>
.mt-12 {
    position: absolute;
    max-width: 100%;
    padding: 0;
    margin: 0;
    
    
    
    .cover {
    position: fixed;
    }   

    .row {
    margin: 0;
    text-align: left;
    color: white;
    margin-left: 10%;
    margin-top: 10%;
    
    h1 {
        margin: 0;
    }
    p {
    font-family: "Roboto light", sans-serif;
    margin-top: -2%;
    }

    }

    .btn-projects {
    margin-right: 5px ;
    margin-top: 5%;
    width: 40%;
    }

    .btn-linkedin {
    margin-top: 5%;
    width: 10%;
    }
}


/* button {
    width: 100%;
}
.info-enter-active {
    transition: all .3s ease;
}

.info-leave-active {
    transition: all .3s;
}

.info-enter, .info-leave-to {
    transform: translateY(-10px);
    opacity: 0;
}


.more-enter-active {
    transition: all .3s ease;
}

.more-leave-active {
    transition: all .3s;
}

.more-enter, .more-leave-to {
    transform: translateY(-10px);
    @keyframes more {
        0% {
            opacity: 100%;
        }
        100% {
            opacity: 0%;
        }

    }
}*/
</style>
