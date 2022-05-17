<template>
  <footer>
    <div class="top">
      <div class="col">
        <ul>
          <li class="list-title">DC COMICS</li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
        </ul>
        <ul>
          <li class="list-title">SHOP</li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
        </ul>
      </div>
      <div class="col">
        <ul>
          <li class="list-title">DC</li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
        </ul>
      </div>
      <div class="col">
        <ul>
          <li class="list-title">SITES</li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
          <li><a href="">Link</a></li>
        </ul>
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
            <li>
              <img src="../assets/img/footer-facebook.png" />
            </li>
            <li>
              <img src="../assets/img/footer-twitter.png" />
            </li>
            <li>
              <img src="../assets/img/footer-youtube.png" />
            </li>
            <li>
              <img src="../assets/img/footer-pinterest.png" />
            </li>
            <li>
              <img src="../assets/img/footer-periscope.png" />
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
