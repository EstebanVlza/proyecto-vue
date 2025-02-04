<template>
<Header></Header>
  <div class="container">
    <Sidebar></Sidebar>
    <div class="content">
      <router-view></router-view>
    </div>
  </div>
</template>
<script setup>
import Sidebar from '@/components/_Sidebar.vue';
import Header from '@/components/_Header.vue';
</script>
<style>
  .container{
    display: flex;
  }
  .content{
    flex: 1;
    padding: 20px;
  }
</style>
