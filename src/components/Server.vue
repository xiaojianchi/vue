<template>
  <div>
    <li class="list-group-item" @click="showServer">Server#{{server.id}}</li>
  </div>
</template>

<script>
  import {serverBus} from "../main";

  export default {
       props:['server'],
       methods:{
           showServer(){
               serverBus.$emit('show',this.server);
           }
       }
    }
</script>

<style scoped>
 div>li {
   cursor: pointer;
 }
</style>
