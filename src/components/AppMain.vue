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
  import AppSelect from './AppSelect.vue';
  import { store } from '../store.js'
  import axios from 'axios';
  export default {
    data(){
        return{
            store,
            listCard:[],
        }
    },
    name: "AppMain",
    components:{
        AppCardList,
        AppSelect  
    },
    created(){
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then( (response) => {
        console.log(response.data.data);
        this.store.listCard = response.data.data
    })
    .catch(function (error) {
        console.log(error);
    })
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