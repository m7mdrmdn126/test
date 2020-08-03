<template>
  <div id="app">
    <Header
      :students_num="students_num"
    ></Header>

    <test
      :increment="increment"
    ></test>
  </div>
</template>

<script>
import test from './components/test.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    test,
    Header
  },
  data() {
    return {
      students_num: 4,
    }
  },
  methods: {
    increment: function(act_num){
      this.students_num = act_num;
      console.log(this.students_num)

    }
  },
}
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
