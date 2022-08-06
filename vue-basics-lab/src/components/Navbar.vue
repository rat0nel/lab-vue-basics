<template>
  <nav class="navbar">
    <div><router-link to="/">Home</router-link></div>
    <div><router-link to="/about">About</router-link></div>
    <div><router-link to="/contact">Contact</router-link></div>
    <button @click="hideUnhide" v-if="signedIn">Log In</button>
    <button @click="hideUnhide" v-if="!signedIn">Log Out</button>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      signedIn: true
    }
  },
  methods:{
    hideUnhide() {
      if (this.signedIn === false) {
        this.signedIn = true;
      }else{
        this.signedIn = false
      }
      }
    },
  };
</script>

<style>
    .navbar {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        border-style:ridge;
        
    }
    button{
      background-color: bisque;
    }
</style>