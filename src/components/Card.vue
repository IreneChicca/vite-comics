<script>
export default {
  data() {
    return {};
  },

  props: {
    comic: Object,
  },

  name: "Card",
};
</script>
<template>
  <div class="col-2 pt-5">
    <img :src="comic.thumb" alt="" class="p-2" />
    <p class="m-0">{{ comic.series }}</p>
  </div>
</template>
<style lang="scss" scoped>
img {
  //  aspect-ratio: 1/1;

  width: 200px;
  height: 200px;
}
</style>
