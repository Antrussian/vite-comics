<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';
import AppSocialLink from './components/AppSocialLink.vue';



export default {
  name: 'App',

  components:{
    AppHeader,
    AppMain,
    AppNav,
    AppFooter,
    AppSocialLink,



  }
}
</script>

<template lang="">
  <AppHeader/>
  <AppMain/>
  <AppNav/>
  <AppFooter/>
  <AppSocialLink/>




</template>

<style lang="scss">
  @use '../node_modules/bootstrap/scss/bootstrap.scss' as *;
  @use './styles/general.scss' as *;
  @use './styles/partials/variables' as *;
  @use './styles/partials/mixins' as *;
  

</style>