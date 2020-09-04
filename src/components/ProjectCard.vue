<template>
    
<div>
    <b-card
    :title="name"
    overlay
    img-src="https://2.bp.blogspot.com/-L_goFZl2GJ0/WBrOXSnrHGI/AAAAAAAACxw/fGhJehW07kc8I4pjHvC3F0Wow-qAQchzwCLcB/s1600/laravel-5-crud-with-vue-js.png"
    img-alt="Project 01"
    img-top
    tag="article"
    style="max-width: 25rem;"
  >
    <b-card-text>{{ details }}</b-card-text>

    <b-button href="#" variant="primary">Go to the site</b-button>
    </b-card>
    </div>
</template>

<script>
    export default {
        props: 
            ["name", "id", "details"]
        
    }
    
</script>

<style scoped>

</style>