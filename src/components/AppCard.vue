<template>
<div class="card">
   <img :src="image" class="img-fluid" alt="...">
    <div class="card-body">
    <h5 class="card-title">{{ title }}</h5>
    <p class="card-text">{{ type }}</p>
    <p class="card-text">{{ archetype }}</p>
  </div>
</div>
  </template>
  
  
  
  <script>
  import { store } from '../store';
  export default {
    name: "AppCard",
    props:{
        title : String,
        type : String,
        image : String,
        archetype: String
    }
  }
  </script>
   
  
  <style lang="scss">
  .card{
     width: calc(100% / 5 - 1rem) !important;
     margin-right: 1rem;
     margin-bottom: 3rem;

     img{
      width: 100%;
     }

     h5{
      font-size: 0.9rem;
     }

     p{
      font-size: 0.85rem;
     }
  }
  </style>