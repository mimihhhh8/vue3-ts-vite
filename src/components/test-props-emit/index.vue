<template>
  <p>{{props.msg}}</p>
  <button @click="handleClick">点击我调用父组件方法</button>
</template>
<script setup lang="ts">
  const props = defineProps({
    msg:{
      type:String,
      default:()=>"默认值"
    }
  })

  const emit = defineEmits(["on-change"])
  const handleClick = ()=>{
    emit("on-change","父组件方法被调用了")
  }
</script>
