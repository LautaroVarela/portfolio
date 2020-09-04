<template>
    <b-navbar toggleable="md" type="dark" variant="primary">

    <b-navbar-toggle target="nav-collapse" class="text-light" ></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="d-md-flex d-block flex-row mx-md-auto">
        <b-nav-item class="home" :to="{ name: 'home' }" exact>Home</b-nav-item>
        <b-nav-item class="projects" :to="{ name: 'projects' }">Projects</b-nav-item>
        <b-nav-item class="contact" :to="{ name: 'contact' }">Contact</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<style scoped>



</style>