<template>
  <div class="item" @click="itemClick" v-html="htm"></div>
</template>

<script>
export default {
  props: ['cityName'],
  data(){
    return {}
  },
  methods: {
    itemClick(){
      this.$emit('itemClick', this.cityName)
    }
  },
  computed: {
    htm(){
      let city = this.cityName
      let res = city.replace(this.$attrs.highText, `<span style="color: #409EFF">${this.$attrs.highText}</span>`)
      return res
    }
  }
}
</script>

<style lang="less">
 .item {
    width: 400px;
    height: 30px;
    // background: rgb(199, 198, 198);
    font-weight: 500;
    text-align: left;
    line-height: 30px;
    padding: 2px 0;
    color: #606266;
 }
 .item:hover{
   color: #409EFF;
   cursor: pointer;
 }
</style>