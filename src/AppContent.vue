<script>
export default {
  data() {
    return {};
  },
};
</script>
<template>
  <div class="content">
    <div class="hero"></div>
    <h1>content goes here</h1>
  </div>
</template>
<style lang="scss" scoped>
.content {
  background-color: #181818;
  color: #ffffff;

  .hero {
    background-image: url(./assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 350px;
  }
}
</style>
