<template>
  <div class="test-container">
  <Empty/>
  </div>

</template>

<script>
import Empty from "./"
export default {
    components: {
        Empty,
    }
}
</script>

<style>
.test-container {
  width: 300px;
  height: 300px;
  border: 1px solid red;
  margin: 0 auto;
  position: relative;
}
</style>