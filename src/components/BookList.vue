<template>
  <div> 
      <h1> {{title}} 
          <ul>
              <li v-for="book in books">{{book.title}}:{{book.author}} </li>
             
          </ul>
      </h1>
  </div>
</template>

<script>
import BookItem from './components/BookItem';
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