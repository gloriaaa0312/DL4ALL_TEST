<template>
    <h1>{{ message }}</h1>
    <!-- <p>{{ test.split('').reverse().join('') }}</p> -->
    <div v-bind:class="a">test</div>
  </template>
  
  <script>
  
  export default {
    data() {
      return {
        message: 'Hello Vue',
        test:'test',
        a:'?'
      };
    }
  }
  </script>
  