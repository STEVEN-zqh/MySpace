<template>
  <div class="avatar-container">
    <img
      class="img-container"
      :src="url"
      :style="{ width: size + 'px', height: size + 'px' }"
    />
  </div>
</template>

<script>
export default {
  props: {
    url: {
      type: String,
      required: true,
    },
    size: {
      type: Number,
      default: 100,
    },
  },
};
</script>

<style scoped>
.img-container {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
}

</style>
