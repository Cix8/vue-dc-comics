<template>
  <li>
    <div class="img-container">
      <img
        :src="seriesObj.thumb"
        :alt="seriesObj.type + ': ' + seriesObj.series"
      />
    </div>
    <div class="title">
      <h3>{{ seriesObj.series }}</h3>
    </div>
  </li>
</template>

<script>
export default {
  name: "SingleSeries",
  props: {
    seriesObj: Object,
  },
};
</script>

<style lang="scss" scoped>
li {
  $width: calc(((100vw - 320px) / 6) - 20px);

  width: $width;
  margin: 10px;
  padding: 5px;

  .img-container {
    width: $width;
    height: $width;
    margin-bottom: 10px;

    img {
      object-fit: cover;
      object-position: 60% top;
    }
  }
}
</style>
