<template>
  <nav>
    <ul>
      <li v-for="(link, index) in navLinks" :key="index">
        <div class="img-container">
          <img :src="require('../assets/img/buy-' + link.image)" />
        </div>
        <div class="text">
          <span>{{ link.text }}</span>
        </div>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "ShopNav",
  data: function () {
    return {
      navLinks: [
        {
          image: "comics-digital-comics.png",
          text: "digital comics",
        },
        {
          image: "comics-merchandise.png",
          text: "dc merchandise",
        },
        {
          image: "comics-subscriptions.png",
          text: "subscription",
        },
        {
          image: "comics-shop-locator.png",
          text: "comics shop locator",
        },
        {
          image: "dc-power-visa.svg",
          text: "dc power visa",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
nav {
  width: 100%;
  height: 130px;
  background-color: #0282f9;
  padding: 0 150px;

  ul {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;

    li {
      display: flex;
      align-items: center;

      .img-container {
        width: 50px;
        height: 50px;
        margin-right: 10px;
      }

      .text {
        text-transform: uppercase;
      }
    }
  }
}
</style>
