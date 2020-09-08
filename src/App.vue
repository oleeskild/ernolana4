<template>
  <div id="app">
    <h2> Er Nolan A4?</h2>

<transition name="fade">
    <h1 v-if="show"> NEI STIAN.</h1>
</transition>
<transition name="fade">
    <h1 v-if="show2">NEI!</h1>
</transition>
<transition name="fade">
    <h1 v-if="show3">Stian... NEI</h1>
</transition>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      show: false,
      show2: false,
      show3: false
    }
  },
  mounted: function(){
    this.show=true;
    setTimeout((()=>this.show2=true), 1000)
    setTimeout((()=>this.show3=true), 3000)
  }
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
h1 {
  font-size: 92px;
}
h2 {
  font-size: 64px;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 3s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.fade2-enter-active, .fade-leave-active {
  transition: opacity 3s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
