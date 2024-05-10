<template>
  <div class="imageloader-container">
    <img v-if="!ererythingDone" class="placeholder" :src="placeholder" alt="" />
    <img
      @load="handleLoad"
      class="origin"
      :src="src"
      alt=""
      :style="{ opacity: originopacity, transition: `${duration}ms` }"
    />
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    placeholder: {
      type: String,
      required: true,
    },
    duration: {
      type: Number,
      required: false,
      default: 1000,
    },
  },
  data() {
    return {
      originLoaded: false,
      ererythingDone: false,
    };
  },
  methods: {
    handleLoad() {
      this.originLoaded = true;
      setTimeout(() => {
        this.ererythingDone = true;
      this.$emit("load")}, this.duration);
    },
  },

  computed: {
    originopacity() {
      return this.originLoaded ? 1 : 0;
    },
  },
};
</script>

<style lang="less" scoped>
@import "~@/styles/mixin.less";
.imageloader-container {
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  img {
    .self-fill();
    object-fit: cover;
  }
  .placeholder {
    filter: blur(2vw);
  }
}
</style>
