<template>
  {{ person.name + " " + person.email }}
  <div class="hello">
    <input type="text" v-model="koukou.name">
    <input type="text" v-model="koukou.email">
    <h1>{{ msg }}</h1>

  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data(){
    return{
      koukou:this.person
    }
  },
  props: {
    msg: {type: String, default: "Test 2Way Binding", required: false },
    person: {type:Object}  
      
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
