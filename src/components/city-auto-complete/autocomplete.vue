<template>
  <div class="auto">
    <input type="text" autofocus placeholder="Search City Name" v-model="inputValue" @input="filterList">
    <notice :cityList="showList" @fillVal="fillVal" :highText="inputValue"></notice>
  </div>
</template>

<script>
import notice from './notice'
export default {
  components:{notice},
  data(){
    return {
      inputValue: '',
      showList:[],
      allList: ['北京', '南京', '上海', '西京', '武汉', '西安', '重庆', '天津', '北安', '铜川', '南宁', '宁夏', '银川', '长沙', '北京东']
    }
  },
  created(){
    this.showList = this.allList
  },

  methods: {
    filterList(){
      this.showList = this.allList.filter(item => {
        return item.includes(this.inputValue)
      })
    },
    fillVal(val){
      this.inputValue = val
      this.showList = []
    }
  }
}
</script>

<style lang="less">
  input {
    height: 30px;
    width: 400px;
    border: none;
    border-bottom: 1px rgb(80, 79, 79) solid;
    font-size: 16px;
    color: rgb(87, 87, 87);
    // font-weight: bold;
  }
  input:focus-visible {
    outline: 0px;
  }
</style>