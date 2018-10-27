<template>
  <div>
    <ListItem v-bind:job="job" />
    <div v-html="job.detailContent"></div>
  </div>
</template>

<script>
  import JobList from '../data/JobList.json';  
  import ListItem from './common/ListItem.vue';

  export default {
    name: 'Detail',
    components: {
      ListItem
    },

    data() {
      return {
        job: JobList.result.items.find(job => job.jobId === this.$route.params.id)
      }
    }
  }
  
</script>