<template>
  <div class="col-xs-12 col-sm-6">
    <ul class="list-group">
      <Server v-for="server in servers" :key="server.id"
              :server="server"
             ></Server>
    </ul>
  </div>
</template>

<script>
  import Server from './Server.vue';

  export default {
      components:{
          Server
      },
      data(){
          return {
            servers:[
                {id:1,status:'Normal'},
                {id:2,status:'OnNormal'},
                {id:3,status:'InNormal'},
                {id:4,status:'UnNormal'}
            ]
          };
      }
  }
</script>

<style scoped>

</style>
