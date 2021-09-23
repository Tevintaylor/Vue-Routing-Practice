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
      <h2>User Profile</h2>
      <ul>
        <li v-for="(id, index) in userIds" :key="index">
          <router-link :to="{ name: 'ViewProfile',params:{ user_id: id}}">
            <span>Profile {{ id }} </span>
          </router-link>
        </li>
      </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      userIds: ['1','2','3','4'],
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
