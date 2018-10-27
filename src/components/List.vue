<template>
  <div>
    <input v-model="searchTerm" type="text" value="" placeholder="Şehir ya da isme göre ara"/>
    <ListItem v-for="job in filteredList" v-bind:job="job" />
  </div>
</template>

<script>
  import JobList from '../data/JobList.json';
  import ListItem from './common/ListItem.vue';

  export default {
    name: 'List',
    components: {
      ListItem
    },

    data() {
      return {
        List : JobList.result.items,
        searchTerm : ''
      }
  },
  methods: {
    searchIn(value, term) {
      let regexTerm = new RegExp(term, "i");
      return value.search(regexTerm) != -1;
    }
  },
  computed: {
    filteredList() {
      const searchTerm = this.searchTerm;
      const List = this.List;
      return List.filter(item => this.searchIn(item.positionName, searchTerm) || this.searchIn(item.cityName, searchTerm) );
    }
  }
  }
</script>

<style scoped lang="less">
  input {
    border: 1px solid #e0e0e0;
    margin-bottom: 1rem;
    padding: .5rem;
    width: 100%;
  }
</style>