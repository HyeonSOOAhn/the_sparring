<template>
  <div>
    <Login/>
  </div>
</template>

<script>
import Login from "./components/Login.vue";

export default {
  name: 'App',
  components: {
    Login,
  }
}
</script>

<style>
html { 
  background: url("./assets/main.jpg"); 
}
</style>
