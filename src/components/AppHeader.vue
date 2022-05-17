<template>
  <header>
    <div class="col-left">
      <img src="../assets/img/dc-logo.png" />
    </div>
    <nav class="col-right">
      <ul>
        <li v-for="(link, index) in menuLinks" :key="index">
          {{ link.text }}
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data: function () {
    return {
      menuLinks: [
        {
          url: "#",
          text: "characters",
          active: false,
        },
        {
          url: "#",
          text: "comics",
          active: false,
        },
        {
          url: "#",
          text: "movies",
          active: false,
        },
        {
          url: "#",
          text: "tv",
          active: false,
        },
        {
          url: "#",
          text: "games",
          active: false,
        },
        {
          url: "#",
          text: "collectibles",
          active: false,
        },
        {
          url: "#",
          text: "videos",
          active: false,
        },
        {
          url: "#",
          text: "fans",
          active: false,
        },
        {
          url: "#",
          text: "news",
          active: false,
        },
        {
          url: "#",
          text: "shop",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
header {
  heigth: 130px;
  background-color: #ffffff;
  display: flex;
  justify-content: space-between;
  padding: 0 150px;

  .col-left {
    width: 100px;
    padding: 15px 0;
  }

  .col-right {
    ul {
      display: flex;
      height: 100%;

      li {
        line-height: 130px;
        text-transform: uppercase;
        font-weight: 500;

        &:not(li:first-child) {
          margin-left: 30px;
        }
      }
    }
  }
}
</style>
