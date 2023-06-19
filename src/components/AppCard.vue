<template>
    <div>
      <div class="image-container">
        <!-- <img :src="image" alt="title"> -->
      </div>
    </div>
  </template>
  
  
  
  <script>
  export default {
    name: "AppCard",
    props:{
        title : String,
        type : String,
        image : String,
    }
  }
  </script>
   
  
  <style lang="scss">
  
  </style>