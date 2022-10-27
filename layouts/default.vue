<template>
  <div>
    <customHeader />
    <div class="main">
      <nuxt />
    </div>
  </div>
</template>

<script>
  import customHeader from '@/components/customHeader'
  export default {

  }
</script>

<style>
  .main {
    padding-top: 50px;
  }
</style>
