<template>
  <div class="listItem">
    <p class="title"><router-link :to="{ name: 'Detail', params: { id: job.jobId } }">{{job.positionName}}</router-link></p>
    <p>{{job.companyName}}</p>
    <p>{{job.cityName}}</p>
  </div>
</template>

<script>
export default {
  name: 'ListItem',
  props: {
    job: Object
  }
}
</script>

<style scoped lang="less">
  p {
    line-height: 1rem;
  }
  .listItem {
    border-bottom: 1px solid #e0e0e0;
    padding: 1rem 0;
    margin-bottom: 1rem;
  }

  .title {
    font-size: 1.4rem;
    text-decoration: none;

    a{
    color: #333;
    }
  }
</style>