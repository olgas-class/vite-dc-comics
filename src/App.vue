<script>
import AppHeader from './components/AppHeader.vue';
import ComicsList from './components/ComicsList.vue';
import AppIcons from './components/AppIcons.vue';

export default {
  components: {
    AppHeader,
    ComicsList,
    AppIcons
  }
}
</script>

<template>
  <AppHeader />

  <main>
    <ComicsList />
    <AppIcons />
  </main>

</template>

<style lang="scss">
@use "./styles/general.scss";
</style>