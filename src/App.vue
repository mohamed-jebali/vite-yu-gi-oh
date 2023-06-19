<script>
import AppHeader from './components/AppHeader.vue'
import AppSelect from './components/AppSelect.vue'
import AppMain from './components/AppMain.vue'
import './styles/general.scss'
import { store } from './store'
import axios from 'axios';

export default{
  data() {
    return {
      store,
    }
  },
  name:"App",
  components:{
    AppHeader,
    AppSelect,
    AppMain,
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

<template>
  <AppHeader/>
  <AppSelect/>
  <AppMain/>
</template>

<style lang="scss">
@import "./bootstrap/scss/bootstrap";
body{
    background-color: #d48f38;
  }

</style>
