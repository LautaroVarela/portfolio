<template>
  <div id="app">
    
    <Nav/>
    <transition  name="view">
    <router-view/>
    </transition>

    <Footer/>

  </div>
  
    
</template>

<script>


import Nav from '@/components/Nav.vue'
import Footer from '@/components/Footer.vue'

export default {
    components: {
        Nav,
        Footer
    }
    
}
</script>
<style scope>

body, html {
    width: 100%;
    height: auto;
}

h1{
    margin: 3%;
    width: 100%; 
    padding-bottom: 5%;
}
p {
    position:relative;
}
  
.page {
  display: block;
  position: fixed;
}
.view-enter-active, .view-leave-active {
transition: opacity 0.5s ease-in-out, transform 0.5s ease;
}

.view-enter-active {
  transition-delay: 0.3s;
}

.view-enter{
  opacity: 0;
  transform: translateY(-100px);
}

.view-enter-to{
  opacity: 1;
  transform: translateY(0px);
}

.view-leave {
opacity: 1;
  transform: translateY(0px);
}

.view-leave-to {
opacity: 0;
  transform: translateY(100px);
}

</style>
