<template>
  <div id="app">
    <h1>{{ title }}</h1>
  <Button @click="increment" outlined>Click me</Button>
  <directives-test/> 
    </div>
</template>

<script>
import Button from '../components/Button.vue'
import DirectivesTest from '../components/DirectivesTest.vue'

export default {
  name: 'App',
  components: {
    Button,
    DirectivesTest
  },
  data() {
    return {
      amountOfClicks:0
    }
  },
  computed: {
    title (){
      return `Amount of clicks ${this.amountOfClicks}`
    }
  },
  methods: {
    increment() {
      this.amountOfClicks += 1
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


</style>
