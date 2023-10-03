<script >
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader,

  }
}
</script>

<template>
  <AppHeader />
  <div class="jumbo">
  </div>
</template>

<style lang="scss" scoped>
.jumbo {
  height: 800px;
  background-image: url(https://image.api.playstation.com/vulcan/ap/rnd/202206/0307/wIVJREWyBg8SyXvXYuBPG6je.png);
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
