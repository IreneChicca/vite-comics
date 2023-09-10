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
    <div class="footer-list">
      <div class="container d-flex justify-content-between pos-rel">
        <div class="d-flex">
          <div class="col-4">
            <h5>DC COMICS</h5>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>TV</li>
              <li>Games</li>
              <li>Videos</li>
              <li>News</li>
            </ul>
            <h5>SHOP</h5>
            <ul>
              <li>Shop DC</li>
              <li>Shop DC Collectibles</li>
            </ul>
          </div>
          <div class="col-4">
            <h5>DC</h5>
            <ul>
              <li>Terms of Use</li>
              <li>Privacy</li>
              <li>Subscriptions</li>
              <li>Shop Helps</li>
              <li>Ad Choices</li>
              <li>Advertising</li>
              <li>Jobs</li>
              <li>Subscriptions</li>
              <li>Ratings</li>
              <li>Shop Helps</li>
              <li>Contact Us</li>
            </ul>
          </div>
          <div class="col-4">
            <h5>SITES</h5>
            <ul>
              <li>DC</li>
              <li>MAD Magazine</li>
              <li>DC Kids</li>
              <li>DC Universe</li>
              <li>DC Power Visa</li>
            </ul>
          </div>
        </div>

        <div class="">
          <img src="./assets/img/dc-logo-bg.png" alt="" class="bglogo" />
        </div>
      </div>
    </div>
    <div class="footer-link"></div>
  </footer>
</template>
<style lang="scss" scoped>
.footer-nav {
  background-color: #0282f9;
  color: #ffff;
}

.footer-list {
  background-image: url(./assets/img/footer-bg.jpg);
  height: 400px;
  overflow: hidden;

  .col-4 {
    color: #ffff;
  }
  ul {
    padding: 0;
  }
  li {
    color: #8b8d8d;
  }

  .bg-logo {
  }
}

.pos-rel {
  position: relative;
}
</style>
