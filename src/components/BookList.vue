<template>
  <div> 
      <h1> {{title}} </h1>
  </div>
</template>

<script>
export default {
data() {
    return {
        title: "All Books",
    }
}
}
</script>

<style scooped>
h1, h2 {
    font-weight: normal;
}
</style>