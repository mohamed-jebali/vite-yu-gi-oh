<script>
import AppHeader from './components/AppHeader.vue'
import AppSelect from './components/AppSelect.vue'
import AppMain from './components/AppMain.vue'
import AppCard from './components/AppCard.vue'
import './styles/general.scss'

export default{
  name:"App",
  components:{
    AppHeader,
    AppSelect,
    AppMain,
    AppCard
  }

}
</script>

<template>
  <AppHeader/>
  <AppSelect/>
  <AppMain/>
  <AppCard/>
</template>

<style lang="scss">
@import "./bootstrap/scss/bootstrap";

</style>
