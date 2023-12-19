<template>
    <main class="row bg-dark">
      <section class="content-section col-12  d-flex align-items-center">
        <h1 class="text-white text-start col-9 p-5">Content is here</h1>
      </section>
    </main>
  </template>
  
  <script>
  export default {
    name: 'AppMain',
    data() {
      return {
       
      };
    },
  }
  </script>
  
  <style lang="scss" scoped>
  @use '../styles/partials/variables' as *;
  @use '../styles/partials/mixins' as *;
  
  main {
    @include flex(row, center, stretch);
  }
  
  section.content-section {
    height: 200px; 
    justify-content: center;
  }
  </style>
  