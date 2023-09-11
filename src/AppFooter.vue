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

      socialLinks: ["fb.png", "twit.png", "yt.png", "pint.png", "fi.png"],
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
      <div class="container d-flex justify-content-between">
        <div class="d-flex pt-4">
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

    <div class="footer-social-link">
      <div
        class="d-flex justify-content-between align-items-center container pt-5 pb-5"
      >
        <div>
          <button class="p-2">SIGN-UP NOW!</button>
        </div>

        <div class="d-flex align-items-center">
          <h4 class="me-3 m-0">FOLLOW US</h4>
          <div v-for="(link, i) in socialLinks">
            <img :src="pathImg(socialLinks[i])" alt="" class="p-2" />
          </div>
        </div>
      </div>
    </div>
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
}

.footer-social-link {
  background-color: #303030;

  button {
    background-color: #303030;
    color: #ffff;
    border: 2px solid #0086fc;
  }

  h4 {
    color: #0086fc;
  }
}
</style>
