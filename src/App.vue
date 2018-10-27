<template>
  <div class="appContainer">  
    <Header />
    <div class="container">
      <div class="row">
        <div class="col-md-6 mx-auto">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/common/Header.vue';
import List from './components/List.vue';

export default {
  name: 'app',
  components: {
    Header,
    List
  }
}
</script>

<style scoped lang="less">
  .appContainer{
   @media screen and (max-width: 576px) {
     padding-left: 15px;
     padding-right: 15px;
     margin-top: 1.5rem;
     margin-bottom: 1.5rem;
   } 
  }
  .container {
    border: 1px solid #e0e0e0;
    margin-top: 1rem;
    padding : 2rem 0;
    @media screen and(max-width: 576px) {
      padding: 1rem;
    }
  }
</style>