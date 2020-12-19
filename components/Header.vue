<template>
 <div class="mb-3">
  <b-navbar toggleable="lg" class="navbar"  variant="info" >
    <b-navbar-brand tag="b-nav-item" to="/">
              <b-avatar variant="info" src="@/static/logo.png"  size="6rem"></b-avatar>
    </b-navbar-brand>
 

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
    
<b-navbar-nav class="m-auto">
      <nuxt-link tag="b-nav-item" to="/">Main Page</nuxt-link>
       <nuxt-link tag="b-nav-item" to="/galery">Gallery</nuxt-link>
      <nuxt-link tag="b-nav-item" to="/about">About</nuxt-link>
      
    </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
    export default {
        
    }
</script>

<style  scoped>
.bg-info{
    background-color: #ccb5a4!important;
}
li.nav-item {
    font-size: 2rem;
}
</style>