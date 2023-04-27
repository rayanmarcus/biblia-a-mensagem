<template>
  <div>
    <div v-for="(book, index) in books" :key="index">
      <h3>{{ book.title }} | Chapters: {{ book.chapters }}</h3>
    </div>
  </div>
</template>

<script>
import books from '@/assets/the-message-the-bible/the-message-the-bible-books.json'

export default {
  name: 'HomePage',
  data() {
    return {
      books: books.slice(0, 20)
    }
  },
}
</script>
<style scoped>
h3{
  color: #fff;
}
</style>
