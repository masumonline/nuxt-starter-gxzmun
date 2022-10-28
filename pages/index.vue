<template>
  <h3 class="text-white bg-pink-600 p-5">Hi there</h3>
  <NuxtLink to="login" class="bg-red-600 text-white p-3 mt-2 ml-2">Login</NuxtLink>
  <button @click="runMe" class="bg-red-600 text-white p-3 mt-2 ml-2">Run Now</button>
  <div>{{ results?.title }}</div>
</template>
<script>
export default {
  data(){
    return {
      results: null,
    }
  },
  methods:{
    runMe(){
    fetch('https://jsonplaceholder.typicode.com/todos/1')
  .then(response => response.json())
  .then(json => this.results = json)
  }
  }
}
</script>
