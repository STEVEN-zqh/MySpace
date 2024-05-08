<template>
    <div class="empty-contoiner">
        <Icon type="empty"/>
        <h1>{{text}}</h1>
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

<style>

</style>