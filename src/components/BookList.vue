<template>
  <div> 
      <h1> {{title}} 
          <ul>
              <li v-for="book in books" :key="book in title">{{book.title}}, {{book.author}} </li>
             
          </ul>
      </h1>
  </div>
</template>

<script>
export default {
data() {
    return {
        title: "All Books",
    }
    books:[
 {
     title: 'Self-Reliance', author: 'Ralph Waldo Emerson'
     },
    {
        title: 'American Gods', author: 'Neil Gaiman'
        },
    {
        title: 'Amusing Ourselves to Death', author: 'Neil Postman'
        },
    ]
        
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
li {
    display: block;
    margin: 0, 10 px;

}
</style>