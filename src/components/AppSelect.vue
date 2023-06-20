<template>
    <div class="container mt-4">
      <select class="form-select form-select-sm" aria-label=".form-select-sm example">
        <option selected>Alien</option>
        <option value="1">One</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
      </select>
    </div>
  </template>
  
  
  
  <script>
  export default {
    data() {
      return {
        textSearch:"",
      }
    },
    name: "AppSelect"
    
  }
  </script>
   
  
  <style lang="scss">
  .form-select{
    width: 10% !important;
  }
  </style>