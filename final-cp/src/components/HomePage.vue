<template>
  <div>
    <div v-if="loggedIn">
      <notes/>
    </div>
    <div v-else>
      <welcome-page/>
    </div>
  </div>
</template>

<script>
 import WelcomePage from './WelcomePage';
 import Notes from './Notes';
 export default {
   name: 'HomePage',
   components: {WelcomePage,Notes},
   computed: {
     loggedIn: function() {
       return this.$store.getters.loggedIn;
     },
   },
 }
</script>

<style scoped>
</style>