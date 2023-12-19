<template lang="">
  <header>
    <section class="logo col-4">
    <img src="../assets/img/dc-logo.png" alt="logo">
</section>
      <nav class="navigation col-8">
          <ul>
            <li v-for="link in navLinks" :key="link.content">
            <a>
                {{ link.content }}
            </a>
        </li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
      return {
          navLinks : [
              {
                  content: 'CHARACTERS',
                  url: '#',
                  active: false,
              },

              {
                  content: 'COMICS',
                  url: '#',
                  active: true,
              },

              {
                  content: 'MOVIES',
                  url: '#',
                  active: false,
              },

              {
                  content: 'TV',
                  url: '#',
                  active: false,
              },
              {
                  content: 'GAMES',
                  url: '#',
                  active: false,
              },
              {
                  content: 'COLLECTIBLES',
                  url: '#',
                  active: false,
              },
              {
                  content: 'VIDEOS',
                  url: '#',
                  active: false,
              },
              {
                  content: 'FANS',
                  url: '#',
                  active: false,
              },
              {
                  content: 'NEWS',
                  url: '#',
                  active: false,
              },
              {
                  content: 'SHOP',
                  url: '#',
                  active: false,
              },
          ],
      }
  },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;




header{
  @include flex(row, center, center);

  section.logo{

      @include flex(row, center, center);
    
      padding: 20px;
  }

  nav.navigation > ul{
      @include flex(row, center, center);

      list-style-type: none;

      li{
        margin-right: 10px;
          font-size: 1.1rem;
        
  
      }
 
  }
}
</style>