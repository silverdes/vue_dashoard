<template>
<div class="space-y-5">
  <sidebar />
  <Map />
</div>
</template>

<script>
import Map from './components/Map.vue'
import Sidebar from './components/Sidebar.vue'

export default{
  components:{
    Sidebar,
    Map,
  },
  data(){
    return{

    }
  }
}
</script>

<style>

</style>
