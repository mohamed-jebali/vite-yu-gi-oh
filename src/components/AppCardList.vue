<template>
    <div v-for="card in listCard">
        :
    </div>
</template>



<script>
import AppCard from './AppCard.vue';
// import axios from 'axios';
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
        console.log(response.data.results);
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