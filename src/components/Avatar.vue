<template>
  <img class="avater-img" :src="url" :style="{ width:size+'px', height:size+'px', }" />
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

<style>
.avater-img{
    border-radius: 50%;
    object-fit: cover;
}
</style>
