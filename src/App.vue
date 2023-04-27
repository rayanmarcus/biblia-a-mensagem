<template>
  <div id="app">
    <Particles/>
    <div class="books">
      <Home/>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Particles from "@/components/particles.vue";

export default {
  name: 'App',
  components: {Home, Particles},
}
</script>

<style>
html {
  background: #08121f;
}
body {
  position: relative;
  background: #4c1010;
  height: 100%;
}
.books{
  position: relative;
  height: 100%;
}
</style>
