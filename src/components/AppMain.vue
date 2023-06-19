<template>
        <div class="container mt-4">
            <div class="cards-container">
                <div class="cards-founded mx-auto">
                    <h3>
                        Found 39 Cards
                    </h3>
                    <AppCardList/>
                </div>
            </div>
        </div>
  </template>
  
  
  
  <script>
  import AppCardList from './AppCardList.vue';
  export default {
    data(){
        return{
        }
    },
    name: "AppMain",
    components:{
        AppCardList,  
    }    
  }

  </script>

  
  <style lang="scss">

   .cards-container{
    background-color: white;
    height: 100vh;
    padding: 4rem;
   }
   .cards-founded{
    background-color: #212529;
    color: white;
    padding: 1.5rem;
    width: 90%;
   }


  </style>