<template>
  <div>
    <app-store-grid :data="prints" />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import AppStoreGrid from "~/components/AppStoreGrid.vue";

export default {
  components: {
    AppStoreGrid
  },
  computed: {
    ...mapGetters(["prints"])
  }
};
</script>

<style lang="scss" scoped>
</style>