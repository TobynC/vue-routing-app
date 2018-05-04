<template>
  <div id="navbar">
    <ul>
        <li><router-link :to="{ name: 'Home' }">Home</router-link></li>
        <li><router-link :to="{ name: 'About' }">About</router-link></li>
        <li v-for="userId in userIds" :key="userId">
            <router-link :to="{ name: 'Profile', params: { userId }}">Profile {{ userId }}</router-link>
        </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: 'NavbarComponent',
        data () {
            return {
                userIds: ['1', '2', '3', '4']
            }
  }
}
</script>

<style scoped>
    ul {
    list-style-type: none;
    margin: 0;
    padding: 20;
    overflow: hidden;
    background-color: #222;
    }

    li {
        float: left;
    }

    li a {
        display: block;
        color: white;
        text-align: center;
        padding: 1.2rem 1.2rem;
        text-decoration: none;
    }

    /* Change the link color to #111 (black) on hover */
    li a:hover {
        background-color: #111;
    }
</style>
