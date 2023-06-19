<template>
</template>



<script>
import AppCard from './AppCard.vue';
import axios from 'axios';
import {store} from "../store.js"
export default {
data(){
    return{
        store,
        listCard:[],
    }
},
name: "AppCardList",
components:{
    AppCard  
},
created(){
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
    .then( (response) => {
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error);
    })
}

}

</script>


<style lang="scss">

.cards-founded{
background-color: #212529;
color: white;
padding: 1.5rem;
width: 90%;
}


</style>