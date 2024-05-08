<template>
  <ImageLoader :src="src" :placeholder="placeholder"/>
</template>

<script>
import ImageLoader from "../ImageLoader"
export default {
    components:{
        ImageLoader,
    },
    data () {
        return {
            // src: "src",
            src: "https://www.baidu.com/img/baidu_jgylogo3.gif",
            placeholder:"https://www.baidu.com/img/baidu_jgylogo3.gif"
        }
    }
}
</script>

<style>

</style>