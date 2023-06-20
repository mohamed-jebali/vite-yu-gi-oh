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

}

</script>


<style lang="scss">


.container-cards{
    display: flex;
    flex-wrap: wrap;
    margin: auto;
}


</style>