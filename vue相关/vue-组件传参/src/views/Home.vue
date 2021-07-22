<template>
    <div class="home">
        <div class="box-all">
            <div class="title">第一种：props和$emit</div>
            <son :parentObj="parentObj" @tellFater="fromSon" />
            <div>儿子的回答：{{ sonMessage }}</div>
        </div>
        <div class="box-all">
            <div class="title">第二种：$parent和 $children</div>
        </div>
		<div class="box-all">
            <div class="title">第三种：$attrs和 $listeners</div>
        </div>
		<div class="box-all">
            <div class="title">第四种：$parent和 $children</div>
        </div>
		<div class="box-all">
            <div class="title">第五种：Provide 和 Inject</div>
        </div>
		<div class="box-all">
            <div class="title">第六种：EventBus</div>
        </div>
		<div class="box-all">
            <div class="title">第七种：Vuex</div>
        </div>
		<div class="box-all">
            <div class="title">第八种：observable</div>
        </div>
    </div>
</template>

<script>
import son from "../components/propsAndEmit/index.vue";
export default {
    name: "Home",
    data() {
        return {
            parentObj: {
                title: "来自父组件的问题:你在干啥？"
            },
            sonMessage: ""
        };
    },
    components: {
        son: son
    },
    methods: {
        fromSon(str) {
            this.sonMessage = str;
        }
    }
};
</script>
<style lang="less">
.box-all {
    border: 1px solid #ccc;
    width: 70%;
    min-height: 100px;
    margin: 0 auto;
    overflow: hidden;
    text-align: left;
    padding: 20px;
    margin-bottom: 10px;
    .title {
        font-weight: 600;
        margin-bottom: 20px;
    }
}
</style>
