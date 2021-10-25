
<!-- <script lang="ts">
// 基础用法
export default{
  props:{
    title:{
      type:String,
      default:()=>{
        return '测试信息'
      }
    }
  },

  setup(props:any){
    console.log(props.title)
  }
}


</script> -->

// 二、高级用法
<script setup lang="ts">
// 主要用在父组件给子组件传值的时候
// 不需要导入，默认导出
  const props = defineProps({
    title:{
      type:String,
      default:()=>{return '测试信息2'}
    }
  })

  console.log(props.title)
</script>


<template>

</template>

<style>
/**
 setup语法糖
 * 1、在setup语法糖中导入组件不需要注册申明，直接在视图中使用即可
 * 2、js默认放到页面顶部
 * 3、导入vue文件必须写上文件后缀名.vue，否则ts无法识别文件
 */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
