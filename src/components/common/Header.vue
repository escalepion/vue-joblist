<template>
  <div class="header">
    <div class="container">    
      <div class="row">
        <router-link to="/">Home</router-link>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Header'
  }
</script>

<style scoped lang="less">
  .header {
    background-color: #88108d;
  }

  a {
    color: #ffffff;
    font-size: 2rem;
  }
</style>