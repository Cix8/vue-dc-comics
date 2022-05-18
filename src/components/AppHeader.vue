<template>
  <header>
    <div class="col-left">
      <img src="../assets/img/dc-logo.png" />
    </div>
    <nav class="col-right">
      <ul>
        <li
          v-for="(link, index) in menuLinks"
          :key="index"
          :class="{ active: link.active === true }"
          @click="activeToggle(index)"
        >
          <a>{{ link.text }}</a>
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
          active: true,
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
  methods: {
    activeToggle: function (index) {
      for (let i = 0; i < this.menuLinks.length; i++) {
        if (this.menuLinks[i].active) {
          this.menuLinks[i].active = false;
        }
      }

      this.menuLinks[index].active = true;
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  height: 100px;
  background-color: #ffffff;
  display: flex;
  justify-content: space-between;
  padding: 0 150px;

  .col-left {
    width: 70px;
  }

  .col-right {
    ul {
      display: flex;
      height: 100%;

      li {
        min-width: 30px;
        text-align: center;
        line-height: 100px;
        border-bottom: 5px solid transparent;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 0.8rem;

        &:not(li:first-child) {
          margin-left: 30px;
        }

        &.active {
          color: #0282f9;
          border-bottom-color: #0282f9;
        }
      }
    }
  }
}
</style>
