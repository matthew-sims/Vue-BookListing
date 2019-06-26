<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="book in books">{{ book.title }}: {{ book.author }}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'BookList',
    data: () => {
      const books = [
        {title: 'The Chronicles of Narnia', author: 'C.S. Lewis'},
        {title: 'Harry Potter', author: 'J.K. Rowling'},
        {title: 'Inheritance Cycle', author: 'Christopher Paolini'},
      ];

      return { title: 'All Books' };
    }
  }
</script>

<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  ul li {
    display: block;
    margin: 0 10px;
  }
</style>