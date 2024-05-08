<template>
  <div class="imageloader-container">
    <img :src="src" alt="">
    <img :src="placeholder" alt="">
  </div>
</template>

<script>
export default {
    props: {
        src: {
            type: String,
            required: true
        },
        placeholder:{
            type: String,
            required: true
        },
        duration:{
            type: Number,
            required: false
        }
    }
}
</script>

<style lang="less" scoped>
    .imageloader-container{
        position: relative;
        width: 100px;
        height: 100px;
        img{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
</style>