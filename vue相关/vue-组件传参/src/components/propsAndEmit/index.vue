<template>
  <div class="container">
      <div>{{parentObj.title}}</div>
      <button @click="tellParent">儿子回答父亲</button>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  props:{
      parentObj:{
          type:Object,
          default:{}
      }
  },
  methods:{
      tellParent(){
          this.$emit("tellFater","我在耍泥巴")
      }
  }
}
</script>

<style scoped lang="less">

</style>
