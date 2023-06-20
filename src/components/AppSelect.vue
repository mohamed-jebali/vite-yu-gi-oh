<template>
    <div class="container my-4">
      <select class="form-select form-select-sm" aria-label=".form-select-sm example">
        <option selected v-for="item in filteredList">{{ item.archetype_name }}</option>
      </select>
    </div>
  </template>
  
  
  
  <script>
    import axios from 'axios';
  export default {
    data() {
      return {
        textSearch:"",
        filteredList:[]
      }
    },
    name: "AppSelect",
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {
                this.filteredList = response.data;
                this.filteredList = this.filteredList.slice(0, 21);
                console.log(this.filteredList);
            })
            .catch(function (error) {
                console.log(error);
            })
            .finally(function () {
            });

    }
    
  }
  </script>
   
  
  <style lang="scss">
  .form-select{
    width: 10% !important;
  }
  </style>