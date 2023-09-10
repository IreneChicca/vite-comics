<script>
import AppHeader from "./AppHeader.vue";
import AppFooter from "./AppFooter.vue";
import AppContent from "./AppContent.vue";

export default {
  data() {
    return {
      title: "ciao",
    };
  },

  components: { AppHeader, AppContent, AppFooter },
};
</script>
<template>
  <h1>{{ title }}</h1>
  <AppHeader></AppHeader>
</template>
<style lang="scss">
@use "./style/generals.scss" as *;
</style>
