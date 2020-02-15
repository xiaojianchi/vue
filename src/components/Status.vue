<template>
  <div class="col-xs-12 col-sm-6">
    <p v-if="!server">Select a Server!</p>
    <p v-else>The Server is {{server.id}},Status:{{server.status}}</p>
    <button @click="resetNormal">Reset to Normal</button>
  </div>
</template>

<script>
  import {serverBus} from "../main";

  export default {
      data(){
        return {
            server:null
        }
      },
      created() {
          serverBus.$on('show',(server)=>{this.server = server});
      },
      methods:{
          resetNormal(){
              this.server.status = 'Normal';
          }
      }
  }
</script>

<style scoped>

</style>
