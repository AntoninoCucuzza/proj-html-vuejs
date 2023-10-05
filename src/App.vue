<script >
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue'
import { store } from './store.js';

export default {
  data() {
    return {
      store,

    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter

  }
}
</script>

<template>
  <AppHeader :menu="store.menu" />
  <AppMain />
  <AppFooter :infos="store.infos" :extras="store.extras" :socials="store.socials" />
</template>

<style lang="scss" scoped>
@use './assets/scss/partials/variables' as *;
</style>
