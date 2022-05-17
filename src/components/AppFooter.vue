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
    </div>
    <div class="bottom"></div>
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
  padding: 0 150px;

  .top {
    display: flex;
    padding: 30px 0;
    color: #747779;

    .col {
      margin-left: 50px;

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
  }
}
</style>
