<template>
  <div class="test-container">
    <Layout>
      <template #left>
        <div class="left">Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores deleniti inventore recusandae asperiores tenetur animi distinctio atque quo odio molestiae accusantium similique, quas repellat? Nulla fuga quam sequi voluptas tenetur.</div>
      </template>
      <template>
        <div class="main">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex tempore laboriosam quae ipsum assumenda minima facilis beatae! Veniam laboriosam maiores nulla quo excepturi ipsam dolor eos eaque, ducimus blanditiis exercitationem!</div>
      </template>
      <template #right>
        <div class="right">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Soluta ut repellat mollitia nesciunt officiis deleniti totam nam! Aperiam tempore saepe omnis animi in quam iusto? Excepturi consectetur deleniti perferendis maiores?</div>
      </template>
    </Layout>
  </div>
</template>

<script>
import Layout from "@/components/Layout";
export default {
  components: {
    Layout,
  },
};
</script>

<style scoped lang="less">
.test-container {
  width: 100%;
  height: 800px;
  border: 1px solid black;
  margin: 0 auto;
  white-space: nowrap;
}
.left{
  width: 200px;
  height: 100%;
  background:red;
}
.main{
  width: 100%;
  height: 100%;
  background: green;
}
.right{
  width: 150px;
  height: 100%;
  background: blue;
}

</style>
