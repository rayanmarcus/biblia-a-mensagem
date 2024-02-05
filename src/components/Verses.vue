<template>
  <div class="container-fluid">
    <div class="container">
    </div>
  </div>
</template>

<script>
import verses from '@/assets/the-message-the-bible/the-message-the-bible-books.json'

export default {
  name: 'VersesPage',
  data() {
    return {
      verses: verses,
    }
  },
  mounted() {
    console.log(verses)
  }
}

</script>