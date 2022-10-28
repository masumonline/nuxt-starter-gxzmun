<template>
  <h3 class="text-white bg-pink-600 p-5">Hi there</h3>
  <button @click="runMe">Run Now</button>
  <div>{{ resutls }}</div>
</template>
<script>
export default {
  data(){
    return {
      results: null;
    }
  }
  methods:{
    runMe(){
    fetch('https://jsonplaceholder.typicode.com/todos/1')
  .then(response => response.json())
  .then(json => this.resulrs = json)
  }
  }
}
</script>
