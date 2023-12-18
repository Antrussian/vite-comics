<script>
import AppHeader from './components/AppHeader.vue';

export default {
  name: 'App',

  components:{
    AppHeader,

  }
}
</script>

<template lang="">
  <AppHeader/>

</template>

<style lang="scss">
  @use '../node_modules/bootstrap/scss/bootstrap.scss' as *;
  @use './styles/general.scss' as *;

</style>