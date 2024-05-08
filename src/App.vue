<template>
  <div id="appp">
    <h1>app</h1>
    <Avatar url="http://120.26.131.204/static/upload/2024-3-13-12-55-24-22-832ff.png" :size="100"/>
    <Icon type="qq"/>
    <Pager :total="total" :current="current" @change="handleChangPager($event)"/> 
  </div>
</template>
<script>
import Avatar from "./components/Avatar"
import Icon from "./components/Icon"
import Pager from "./components/Pager"
export default {
  components: {
    Avatar,
    Icon,
    Pager,
  },
  data () {
    return {
      current:1,
      total:302,
    }
  },
  methods: {
    handleChangPager(n){
      console.log('sss');
      
      this.current = n;
    }
  },
}
</script>
<style scoped>
.iconfont{
  color: rgb(0, 255, 128);
  font-size: 24px;
}
</style>
