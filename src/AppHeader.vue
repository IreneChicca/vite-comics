<script>
export default {
  data() {
    return {
      navlinks: [
        "characters",
        "comics",
        "movies",
        "tv",
        "games",
        "collectibles",
        "videos",
        "fans",
        "news",
        "shop",
      ],
    };
  },
};
</script>
<template>
  <nav>
    <div class="nav d-flex justify-content-between p-4 container">
      <div><img src="./assets/img/dc-logo.png" alt="" class="w-50" /></div>
      <ul class="d-flex">
        <li v-for="(link, i) in navlinks" class="p-2 text-uppercase">
          {{ navlinks[i] }}
        </li>
      </ul>
    </div>
  </nav>
</template>
<style lang="scss" scoped>
.nav {
  background-color: #ffffff;
  color: #686a6a;

  li {
    font-weight: 700;

    &:hover {
      color: #0282f9;
      border-bottom: 3px solid #0282f9;
    }
  }

  .active {
    color: #0282f9;
  }
}
</style>
