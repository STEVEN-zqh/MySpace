<template>
  <div class="paper-contoiner" v-if="pageNumber>1">
    <a @click="changePage(1)" :class="{disable:current === 1}">&lt;&lt;</a>
    <a @click="changePage(current-1)" :class="{disable:current === 1}">|&lt;&lt;</a>
    <a @click="changePage(n)" v-for="(n,i) in numbers" :key="i" :class="{active:n === current}">{{ n }}</a>
    <a @click="changePage(current+1)" :class="{disable:current === pageNumber}">&gt;&gt;</a>
    <a @click="changePage(pageNumber)" :class="{disable:current === pageNumber}">&gt;&gt;|</a>
  </div>
</template>

<script>
export default {
    props:{
        current:{
            type: Number,
            default:1,
        },
        total:{
            type: Number,
            default:0,
        },
        limit:{
            type: Number,
            default:10,
        },
        visibleNumber:{
            type: Number,
            default:10,
        }
    },
    computed: {
        pageNumber(){
            return Math.ceil(this.total/this.limit);
        },
        visibleMin(){
            let min=this.current-Math.floor(this.visibleNumber/2);
            if (min<1){
                min=1;
            }
            return min;
        },
        visibleMax(){
            let max=this.visibleMin+this.visibleNumber-1;
            if (max>this.pageNumber){
                max=this.pageNumber;
            }
            return max;
        },
        numbers(){
            let arr=[];
            for(let i=this.visibleMin;i<=this.visibleMax;i++){
                arr.push(i);
            }
            return arr;
        }
    },
    methods: {
        changePage(n){
            if (n<1 || n>this.pageNumber || n===this.current){
                return;
            }
            this.$emit('change',n);
        }
    }
}
</script>

<style lang="less" scoped>
@import "~@/styles/var.less";
.paper-contoiner{
    display: flex;
    justify-content: center;
    margin: 20px 0;
    a{
        color: @primary;
        margin: 0 6px;
        cursor: pointer;
        &.disable{
            color: @lightWords;
            cursor: not-allowed;
        }
        &.active{
            color: @words;
            cursor: text;
            font-weight: bold;
        }
    }
}
</style>