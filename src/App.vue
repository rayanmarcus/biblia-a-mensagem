<template>
  <div id="app">
    <!-- <Particles/> -->
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
  // eslint-disable-next-line vue/no-unused-components
  components: {Home, Particles},
}
</script>

<style lang="scss">
@import './assets/styles/style.scss';

html {
  background: #08121f;
}
body {
  background: #08121f;
  position: relative;
  height: 100%;
}
.books{
  position: relative;
  height: 100%;
}
</style>
