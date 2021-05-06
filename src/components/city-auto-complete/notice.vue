<template>
  <div class="notice">
      <item v-for="(city, i) in cityList" 
        :key="i"
        :cityName="city"
        @itemClick="itemClick"
        ref="item"
        v-bind="$attrs"
        ></item>
  </div>
</template>

<script>
import item from './item.vue';
export default {
  props: ['cityList'],
  components: {item},
  methods:{
    itemClick(val){
      this.$emit('fillVal', val)
    }
  }
}
</script>

<style lang="less">
  .notice {
    width: 400px;
    margin: 0 auto;
    margin-top: 4px;
  }
</style>