<template>
    <main class="row">
      <section class="navigation col-12  d-flex align-items-center">
        <ul class="d-flex align-items-center text-white">
            <li v-for="navItem in navItems">
                <a href="#" class="d-flex align-items-center text-uppercase text-light p-3">
                    <img :src="getImgPath(navItem.src)" :alt="navItem.text"  class="img-nav">
                    <span>{{ navItem.text }}</span>
                </a>
            </li>
        </ul>
  
      </section>
    </main>
  </template>
  
  <script>
  
  export default {
    name: 'AppNav',
    data() {
      return {
        navItems: [
                {
                    text: 'Digital Comics',
                    src: `comics-digital-comics.png`
                },


                {
                    text: 'DC Merchandise',
                    src: `comics-merchandise.png`
                },


                {
                    text: 'Subscriptions',
                    src: `comics-subscriptions.png`
                },


                {
                    text: 'Comic Shop Locator',
                    src: `comics-shop-locator.png`
                },


                {
                    text: 'DC Power Visa',
                    src: `dc-power-visa.svg`
                },
            ]
        }
    },

    methods: {
        getImgPath(imgPath) {
            return new URL('../assets/img/buy-' + imgPath, import.meta.url).href
        }
    }
}



  </script>
  
  <style lang="scss" scoped>
  @use '../styles/partials/variables' as *;
  @use '../styles/partials/mixins' as *;


  .navigation {
    background-color: blue;
    width: 100%;
     justify-content: center;

}
  

.img-nav {
    width: 60px;

}

  main {
    @include flex(row, center, stretch);
  }
  
  section.content-section {
    height: 200px; 
    justify-content: center;
  }
  </style>
  