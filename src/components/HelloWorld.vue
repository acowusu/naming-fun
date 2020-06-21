<template>
  <div class="container">
    <div class="hello jumbotron">
      <h1>{{ msg }}</h1>
      <b-button  v-on:click="getname()" pill class="light" variant="info" size="lg">Click to generate a new username</b-button>
    </div>
    <code>by defacedace</code>
  </div>
</template>

<script>
import animals from "./animals.json";
import adjectives from "./adjectives.json";

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "hello You",
      animals: animals,
      adjectives: adjectives
    };
  },
  created: function () {
    // `this` points to the vm instance
    this.getname()
  },
  methods: {
    getname: function() {
      console.log(this.adjectives.adjectives)
      let adjective = this.adjectives.adjectives[ Math.floor(Math.random() * this.adjectives.adjectives.length)]
      let animal = this.animals.animals[ Math.floor(Math.random() * this.animals.animals.length)]
      this.msg =  "hello " + adjective +" "+ animal
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.hello
  background: #e9fffd
h3 
  margin: 40px 0 0
.light
  background:#7efff5
  border:0
  color:#4b4b4b
ul 
  list-style-type: none
  padding: 0

li 
  display: inline-block
  margin: 0 10px

a 
  color: #42b983

</style>
