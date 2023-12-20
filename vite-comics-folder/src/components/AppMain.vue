<template>
  <main class="row bg-dark">
    <div class="background"></div>

    <section class="content-section col-12 d-flex align-items-center">
      <div class="comics-container d-flex wrap">
        <AppCard
          v-for="comicInfo in json"
          :key="comicInfo.series"
          :thumb="comicInfo.thumb"
          :price="comicInfo.price"
          :series="comicInfo.series"
          :type="comicInfo.type"
        />
      </div>
    </section>
  </main>
</template>

<script>
import AppCard from './AppCard.vue';
import json from '../assets/json/dc-comics.json';

export default {
  name: 'AppMain',
  components: {
    AppCard,
  },
  data() {
    return {
      json,
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.background {
  background-image: url('../assets/img/jumbotron.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 350px;
}

main {
  @include flex(row, center, stretch);
}

section.content-section {
  height: 200px;
  justify-content: center;
}


</style>
