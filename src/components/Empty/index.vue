<template>
    <div class="empty-contoiner">
        <Icon type="empty"/>
        <p>{{text}}</p>
    </div>
</template>

<script>
import Icon from "../Icon";
export default {
    components: {
        Icon,
    },
    props: {
        text:{
            type:String,
            default:'无数据',
            required: false,
        }
    }
}
</script>

<style lang="less" scoped>
@import "~@/styles/mixin.less";
@import "~@/styles/var.less";
.empty-contoiner{
    .self-center();
    color:@gray;
    text-align: center;
}
.icon-container{
    font-size: 72px;
}
</style>