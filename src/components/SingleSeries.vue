<template>
  <li>
    <div class="img-container">
      <img
        :src="seriesObj.thumb"
        :alt="seriesObj.type + ': ' + seriesObj.series"
      />
    </div>
    <div class="title">
      <h5>{{ seriesObj.series }}</h5>
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
      object-position: top;
    }
  }

  .title {
    text-transform: uppercase;
  }
}
</style>
