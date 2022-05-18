<template>
  <div class="list-container">
    <div class="section-title">
      <h2>CURRENT SERIES</h2>
    </div>
    <ul class="series-list">
      <SingleSeries
        v-for="(item, index) in thisArray"
        :key="index"
        :seriesObj="item"
      />
    </ul>
    <div class="btn-container">
      <button class="load-more-btn">LOAD MORE</button>
    </div>
  </div>
</template>

<script>
import SingleSeries from "./SingleSeries.vue";

export default {
  name: "SeriesList",
  components: {
    SingleSeries,
  },
  props: {
    thisArray: Array,
  },
};
</script>

<style lang="scss" scoped>
.list-container {
  position: relative;
  padding: 50px 150px 20px;

  .section-title {
    position: absolute;
    top: 0;
    left: 150px;
    transform: translateY(-50%);

    h2 {
      display: inline-block;
      padding: 10px 20px;
      background-color: #0282f9;
    }
  }

  .series-list {
    display: flex;
    flex-wrap: wrap;
  }

  .btn-container {
    text-align: center;

    .load-more-btn {
      display: inline-block;
      padding: 5px 50px;
      background-color: #0282f9;
      font-weight: 700;
      color: #ffffff;

      &:hover {
        cursor: pointer;
        text-decoration: underline;
      }
    }
  }
}
</style>
