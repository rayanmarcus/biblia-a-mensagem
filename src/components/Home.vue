<template>
  <div class="container-fluid">
    <div class="row mb-3">
      <h1>Bíblia - A Mensagem</h1>
    </div>
    <div class="row">
      <chapters/>
    </div>
  </div>
</template>

<script>
import Chapters from './Chapters.vue'

export default {
  components: { Chapters },
  name: 'HomePage',
}
</script>
<style scoped>
h1{
  color: #d5d5d5;
  font-size: 2.3em;
}
</style>

