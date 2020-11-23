<template>
  <div>
    <h1>
      {{ title }}
    </h1>
    <ul>
      <li v-for="(book, index) in books" :key="index">
        {{ book.title }}: {{ book.author }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'BookList',
  data() {
    return {
      title: 'All Books',
      books: [
        {title: 'Anatomy of State', author: 'Murray M. Rothbard'},
        {title: 'Atlas Shrugged', author: 'Ayn Rand'},
        {title: 'A Short History of Man', author: 'Hans Herman Hoppe'},
      ]
    }
  },
}
</script>
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
  display: block;
  margin: 0 10px;
}
</style>
