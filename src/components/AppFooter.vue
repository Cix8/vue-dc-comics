<template>
  <footer>
    <div class="top">
      <div v-for="(element, index) in linksArray" :key="index" class="col">
        <ul>
          <li class="list-title">{{ element.title }}</li>
          <li v-for="(item, thisIndex) in element.links" :key="thisIndex">
            <a href="">{{ item }}</a>
          </li>
        </ul>
        <template v-if="index == 0">
          <ul>
            <li class="list-title">SHOP</li>
            <li><a href="">Shop DC</a></li>
            <li><a href="">Shop DC Collectibles</a></li>
          </ul>
        </template>
      </div>
      <div class="img-container">
        <img src="../assets/img/dc-logo-bg.png" />
      </div>
    </div>
    <div class="bottom">
      <div class="left">
        <a href="">SIGN-UP NOW!</a>
      </div>
      <div class="right">
        <div class="anchor-container">
          <a href="">FOLLOW US</a>
        </div>
        <div class="icons-container">
          <ul>
            <li v-for="(icon, index) in footerIncosArray" :key="index">
              <img :src="require('../assets/img/footer-' + icon + '.png')" />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      linksArray: [
        {
          title: "DC COMICS",
          links: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "DC",
          links: [
            "Term Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
      footerIncosArray: [
        "facebook",
        "twitter",
        "youtube",
        "pinterest",
        "periscope",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
footer {
  background-image: url("../assets/img/footer-bg.jpg");

  .top,
  .bottom {
    padding: 30px 150px;
  }

  .top {
    display: flex;
    position: relative;
    color: #747779;

    .col {
      &:not(.col:first-child) {
        margin-left: 50px;
      }

      &:first-child {
        ul:first-child {
          margin-bottom: 10px;
        }
      }

      .list-title {
        color: #ffffff;
        font-weight: 700;
        margin-bottom: 5px;
      }
    }

    .img-container {
      position: absolute;
      width: 400px;
      top: 50%;
      right: 20%;
      transform: translate(0, -50%);
    }
  }

  .bottom {
    position: relative;
    z-index: 99;
    display: flex;
    align-items: center;
    background-color: #303030;

    .left,
    .right {
      width: 50%;
    }

    .left {
      color: #ffffff;

      a {
        display: inline-block;
        padding: 10px;
        border: 2px solid #0282f9;
        font-weight: 700;
      }
    }

    .right {
      display: flex;
      justify-content: flex-end;
      align-items: center;

      .anchor-container {
        padding: 10px 0;
        font-size: 1.2rem;
        font-weight: 900;
        color: #0282f9;
      }

      .icons-container {
        ul {
          display: flex;
          padding: 0 20px;

          li {
            margin: 0 10px;
          }
        }
      }
    }
  }
}
</style>
