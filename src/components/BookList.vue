<template>
  <div> 
      <h1> {{title}} </h1>
          <ul>
              <BookItem v-for="book in books" :book='book' ></BookItem>
             
          </ul>
      
      <book-form @addBook='appendBook'/>
  </div>
</template>

<script>
import BookForm from './BookForm';
import BookItem from './BookItem';

export default {
   
    components: {BookItem, BookForm}, 
   
    methods:{
        appendBook(bookTitle, bookAuthor) {
            this.books.push({ title: bookTitle, author: bookAuthor })
        }
    },
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