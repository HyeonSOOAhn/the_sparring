<template>
  <div id="home">
    <div id="login">
        <Login/>
    </div>
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
#home {
  background: url("./assets/main.jpg");
  position: absolute;
  background-size: cover;
  height: 100%; 
  width: 100%; 
}

#login {
  
}


</style>
