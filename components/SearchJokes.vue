<template>
  <form @submit.prevent="onSubmit" >
    <input class="search" type="text" v-model="text" placeholder="Search Jokes..." />
    <input class="button" type="submit" value="Search Jokes" />
  </form>
</template>
<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
      this.text = ''
    },
  },
}
</script>
<style>
form{
    width: 100%;
    display: flex;
    justify-content: space-between;
}
.search{
    max-width: 500px;
    width: 100%;
    height: 30px;
    border-radius: 6px;
}
.button{
    border-radius: 6px;
    background-color: rgb(5, 249, 5);
    color: #fff;
    border-color: #ccc;
}
</style>
