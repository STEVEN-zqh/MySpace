<template>
  <div class="test-container">
    <ImageLoader :src="src" :placeholder="placeholder" @load="handleLoad"/>
  </div>
</template>

<script>
import ImageLoader from "../ImageLoader";
export default {
  components: {
    ImageLoader,
  },
  data() {
    return {
      src: "https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?fit=crop&crop=entropy&w=3456&h=2304",
      placeholder:
        "https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?w=100",
    };
  },
  methods: {
    handleLoad() {
      console.log("handleLoad完成");
    },
  },
};
</script>

<style scoped lang="less">
.test-container {
    width: 600px;
    height: 400px;
    margin: 0 auto;
    border:1px solid red
}
</style>
