<template>
  <h1>RECIPES:</h1>
  <div class="card>
  <div v-for="result in results" v-bind:value="result.title" v-bind:key="result.title">
  <h2>{{result.title}}</h2>
  <img :src = ("{{result.thumbnail}})" />
  <p>{{result.ingredients}}</p>
  <a href=("{{result.href}}")></a>
  </div>
  </div>
</template>




<script>
import axios from 'axios';

  export default {
    name: 'Recipe',
    data() {
      return {
        results: [],
      };
    },
    created: function() {
      axios
        .get("recipepuppy.json")
        .then(res => {
          this.results = res.data;
        })
    }
  }; 
  
</script>


<style>
 h1 {
    margin-bottom: 100px; 
  }
  
  .card{
  
  padding: 50px;
  border: 1px solid black;
  
  }
</style>