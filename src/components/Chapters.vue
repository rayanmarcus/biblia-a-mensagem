<template>
  <div class="container-fluid">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-6 mb-3 text-center">
          <h2>Antigo testamento</h2>
          <div class="col-md-9 mx-auto chapter-card" v-for="(book, index) in oldTestament" :key="index">
            <h3>{{ book.title }}</h3>
            <span class="count-chapter">{{ book.chapters }} caps.</span>
          </div>
        </div>
        <div class="col-lg-6 mb-3 text-center">
          <h2>Novo testamento</h2>
          <div class="col-md-9 mx-auto chapter-card" v-for="(book, index) in newTestament" :key="index">
            <h3>{{ book.title }}</h3>
            <span class="count-chapter">{{ book.chapters }} caps.</span>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-12 p-0 pr-1 pb-1 text-right">
        <footer>
          <span>
            <a href="https://github.com/rayanmarcus" target="_blank" rel="noopener noreferrer">
              by @rayanmarcus
            </a>
          </span>
        </footer>
      </div>
    </div>
  </div>
</template>

<script>
import books from '@/assets/the-message-the-bible/the-message-the-bible-books.json'

export default {
  name: 'HomePage',
  data() {
    return {
      books: books,
      newTestament: [],
      oldTestament: [],
    }
  },
  mounted() {
    console.log(books)
    this.oldTestament = books.slice(0, 39)
    this.newTestament = books.slice(39, 66)
  }
}
</script>
<style lang="scss" scoped>
h2{
  color: #d5d5d5;
  font-weight: 500;
  font-size: 2em;
}
.chapter-card{
  border: 1px solid #18238E;
  border-radius: 8px;
  margin: 0.3em 0;
  padding: 0.5em 2em;
  width: 100%;
  transition: all 0.35s ease-in-out;
  top: 0;
  user-select: none;
  h3 {
    color: #fff;
    margin: 0;
    padding: 0;
    font-weight: 600;
    position: relative;
    display: inline-block;
    background-image: linear-gradient(to right, #3863c2, #b9d7f6);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  h3::after {
    content: '';
    position: absolute;
    bottom: 0px;
    left: 0;
    height: 2px;
    width: 100%;
    border-radius: 50px;
    background: linear-gradient(to right, #06f3ff97, #071167);
    transform-origin: bottom left;
    transform: scaleX(0);
    transition: transform 0.3s ease-out;
  }
  .count-chapter{
    color: #b0b0b0fd;
    font-size: 10px;
    position: absolute;
    top: 2.5px;
    right: 2.5px;
    background-image: linear-gradient(to left, #08121f, #0c55e680);
    border-radius: 50px;
    padding: 0.5px 3px;
    font-weight: 500;
    transition: all 0.5s;
    transform: translateY(-22px);
    opacity: 0;
  }
}
.chapter-card:hover{
  cursor: pointer;
  box-shadow: 0px 0px 2px 0.5px #18238E;
  background: #071167;
  top: -4.5px;
  h3 {
    font-weight: 700;
    background-image: linear-gradient(to left, #7598c0, #edeef0);
  }
  ::after {
    transform: scaleX(1);
  }
  .count-chapter{
    opacity: 1;
    transform: translateY(0);
    font-weight: 900;
  }
}
footer, a{
  font-size: 0.95em;
  color: #556ec3;
  position: relative;
  display: inline-block;
  background-image: linear-gradient(to right, #ffffff, #1c47bb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 600;
}
footer::after {
    content: '';
    position: absolute;
    bottom: 0px;
    left: 0;
    height: 2px;
    width: 100%;
    border-radius: 50px;
    background: linear-gradient(to right, #8579c8, #071167);
    transform-origin: bottom left;
    transform: scaleX(0);
    transition: transform 0.3s ease-out;
}
footer:hover::after {
  transform: scaleX(1);
}
</style>
