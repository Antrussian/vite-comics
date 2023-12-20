<template>
    <article class="card">

        <div class="img-container">
          <h1>{{ series }}</h1>
          <img :src="thumb" :alt="series" :title="series + '\nPrice:' + price">
        </div>
     
   
    </article>
  </template>
  
  <script>
  export default {
    name: 'AppCard',
    props: {
      thumb: String,
      price: String,
      series: String,
      type: String,
    },
  };
  </script>
  
  <style lang="scss">
  @use '../styles/partials/variables' as *;
  
  .card {
    width: calc(100%/6 - 2rem);
    margin: 1rem;
  
    a {
      color: $primary--color;
    }
  
    .img-container {
      margin-bottom: 1rem;
    }

    
  }
  </style>
  