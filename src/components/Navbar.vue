<template>
  <nav id="app">
  <h2>Menu</h2>
      <ul>
        <li>
          <router-link :to="{ name: 'Home'}">Home</router-link>
        </li>
         <li>
          <router-link :to="{ name: 'About'}">About</router-link>
        </li>
         <li>
          <router-link :to="{ name: 'Contact'}">Contact</router-link>
        </li>
      </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {

    }
  }
}
</script>

<style scoped>
nav{
  text-align: center;
}

nav ul{
  padding: 0;
}

nav li{
  display: inline-block;
  list-style-type:none;
  margin:0;
}
</style>
