<template>
  <div>
    {{ person.name + " " + person.email }}
  </div>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld :person="person" />
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
let p = { name: "John", email: "john@doe" };

export default {
  name: "App",
  data() {
    return {
      person: Object.assign({},p,{prop1:"kati", prop2:"itak"})
    };
  },
  components: {
    HelloWorld,
  },

  mounted() {
    console.log(p);
  },
  updated() {
    console.log(p);
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
