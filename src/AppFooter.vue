<script>
export default {
  data() {
    return {
      footerNavLinks: [
        {
          text: "digital comics",
          img: "buy-comics-digital-comics.png",
        },
        {
          text: "dc merchandise",
          img: "buy-comics-merchandise.png",
        },
        {
          text: "subscription",
          img: "buy-comics-subscriptions.png",
        },
        {
          text: "comic shop locator",
          img: "buy-comics-shop-locator.png",
        },
        {
          text: "dc power visa",
          img: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
  methods: {
    pathImg(img) {
      const imgUrl = new URL("./assets/img/" + img, import.meta.url);
      return imgUrl.href;
    },
  },
};
</script>
<template>
  <footer>
    <div class="footer-nav">
      <div class="container d-flex p-5">
        <div
          v-for="(link, i) in footerNavLinks"
          class="d-flex p-3 align-items-center"
        >
          <img :src="pathImg(footerNavLinks[i].img)" alt="" class="w-25" />
          <p class="text-uppercase m-0 p-3">{{ footerNavLinks[i].text }}</p>
        </div>
      </div>
    </div>
    <div class="footer-list"></div>
    <div class="footer-link"></div>
  </footer>
</template>
<style lang="scss" scoped>
.footer-nav {
  background-color: #0282f9;
  color: #ffff;
}
</style>
