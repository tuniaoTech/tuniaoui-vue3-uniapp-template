<script setup lang="ts">
  import { ref } from 'vue'
  import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
  const counter = ref(0)

  const addCounter = () => {
    counter.value++
  }
</script>

<template>
  <view class="content">
    <image class="logo" src="/static/logo.png" />
    <view class="text-area">
      <view class="tn-mr"><TnIcon name="logo-tuniao" /></view>
      <view class="counter">Current Counter: {{ counter }}</view>
    </view>
    <view class="operation">
      <TnButton type="primary" @click="addCounter">Add Counter Value</TnButton>
    </view>
  </view>
</template>

<style lang="scss" scoped>
  .content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .logo {
    height: 200rpx;
    width: 200rpx;
    margin-top: 200rpx;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 50rpx;
  }

  .text-area {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .counter {
    font-size: 36rpx;
  }

  .operation {
    margin-top: 50rpx;
  }
</style>
