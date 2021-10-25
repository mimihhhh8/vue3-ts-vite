

<script setup lang="ts">
import TestPropsEmit from "./components/test-props-emit/index.vue"
import {ref} from 'vue'//提供定义变量

const msg = ref('欢迎学习vite')

const handleChange = (param:string)=>{
  console.log(param)
}
</script>


<template>
<!-- 
  1、@on-change="handleChange" 子组件调用父组件的方法
  2、:msg="msg"父组件给子组件传值
 -->
<TestPropsEmit @on-change="handleChange" :msg="msg"></TestPropsEmit>
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
