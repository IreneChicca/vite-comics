<script>
import AppHeader from "./AppHeader.vue";
import AppFooter from "./AppFooter.vue";
import AppContent from "./AppContent.vue";

export default {
  data() {
    return {};
  },

  components: { AppHeader, AppContent, AppFooter },
};
</script>
<template>
  <AppHeader />
  <AppContent />
  <AppFooter />
</template>
<style lang="scss">
@use "./style/generals.scss" as *;
</style>
