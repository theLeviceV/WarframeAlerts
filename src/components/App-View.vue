<template>
  <div class="container">
    <h1>Welcome to Warframe-Alerts Alpha_v0.1.0</h1>
    <span>{{ dataFromServer }}</span>
  </div>
</template>

<script>
  const axios = require('axios');

  export default {
    data: function() {
      return {
        dataFromServer: 'Waiting...'
      }
    },
    mounted: function() {
      axios.get('http://localhost:8080/dynamic/worldState.php')
        .then(response => {
          this.dataFromServer = response.data;
        })
        .catch(error => {
          console.log(error);
        })
    }
  }
</script>

<style scoped>
  h1 {
    text-align: center;
  }
  .container {
    background: #0D0D0D;
    max-width: 1200px;
    margin: 0px auto;
    padding: 0px 15px;
  }
</style>