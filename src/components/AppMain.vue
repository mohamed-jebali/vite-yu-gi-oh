<template>
        <main class="container mt-4">
            <div class="cards-founded container">
                <h3>
                    Cards Founded 39
                </h3>
            </div>
            <div class="cards-container">
                <AppCardList/>
            </div>
        </main>
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
padding: 4rem;
}

.cards-founded{
    background-color: black;
    color: white;
    padding: 1.5rem;

    h3{
        margin-left: 4rem;
    }
}



</style>