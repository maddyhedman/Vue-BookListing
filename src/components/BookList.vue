<template>
  <div> 
      <h1> {{title}} 
          <ul>
              <BookItem v-for="(book, index) in books" v-bind:book='book' :key="index"></BookItem>
             
          </ul>
      </h1>
  </div>
</template>

<script>

import BookItem from './BookItem.vue';
export default {
    name: 'BookList',
    components: {BookItem},
data() {
    return {
        title: "All Books",
   
    books:[
 {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
    {title: 'American Gods', author: 'Neil Gaiman'},
    {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
    ]
      }   
    }
}
 

</script>

<style scooped>
h1, h2 {
    font-weight: normal;
}

ul {
    list-style-type: none;
    padding: 0;
}


</style>