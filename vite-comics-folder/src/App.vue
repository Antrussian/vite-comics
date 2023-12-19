<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  name: 'App',

  components:{
    AppHeader,
    AppMain,
    AppNav,
    AppFooter,


  }
}
</script>

<template lang="">
  <AppHeader/>
  <AppMain/>
  <AppNav/>
  <AppFooter/>


</template>

<style lang="scss">
  @use '../node_modules/bootstrap/scss/bootstrap.scss' as *;
  @use './styles/general.scss' as *;
  

</style>