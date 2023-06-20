<template>
        <div class="container container-cards">
            <AppCard v-for="item in store.listCard"
            :title="item.name"
            :type="item.type"
            :image="item.card_images[0].image_url"
            :archetypes="item.archetypes"
            />
        </div>
</template>



<script>
import AppCard from './AppCard.vue';
import {store} from "../store.js"
import axios from 'axios';
export default {
data(){
    return{
        store,
    }
},
name: "AppCardList",
components:{
    AppCard,
    store  
},
created(){
    axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
    .then( (response) => {
        console.log(response.data.archetype);
        // this.store.listCard = response.data.data
    })
    .catch(function (error) {
        console.log(error);
    })
}
}

</script>


<style lang="scss">


.container-cards{
    display: flex;
    flex-wrap: wrap;
    margin: auto;
}


</style>