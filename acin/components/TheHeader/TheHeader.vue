<template>
  <header class="main-header">
      <nav class="main-nav">
        <ul class="nav-links">
        <nuxt-link to="/" tag="li" class="nav-link" ><a>All Posts</a></nuxt-link>
         <nuxt-link to="/about" tag="li" class="nav-link" ><a>About</a></nuxt-link>
         <nuxt-link to="/users" tag="li" class="nav-link" ><a>Users</a></nuxt-link>
         <nuxt-link to="/indexProduto" tag="li" class="nav-link" ><a>Produtos</a></nuxt-link>
         </ul>
      </nav>  
      <theSideNavToggle @toggle="$emit('sidenavToggle')"/>
    </header>
</template>
<script>

import TheSideNavToggle from "@/components/TheSideNavToggle";

export default {
  name:"TheHeader",
  components :{
      TheSideNavToggle
  }
}
</script>

<style scoped>
.main-header{
  position:fixed;
  top: 0;
  left:0;
  width:100%;
  background-color: #333;
  height:4.5rem;
}
.main-nav{
  height:100%;
  float: left;
}
.nav-links{
  list-style-type:none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height:100%;
}
.nav-link{
  height:100%;
  display:flex;
  justify-content: center;
  align-items: center;
  margin: 0 1rem;
  padding: 0.3rem;
}
.nav-link a {
  display: block;
  text-decoration: none;
  color: white;
}
.nav-link a:hover,
.nav-link a:active,
.nav-link.nuxt-link-exact-active a {
  color: 3px solid red;
}
.nav-link.nav-link.nuxt-link-exact-active{
  border-bottom:3px solid red;
}

</style>





