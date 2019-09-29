<template>
<div>
<ul class="list-group">
<app-server
 v-for="server in servers"
      :key="server"  :server="server">
</app-server>
</ul>
</div>
</template>
<script>
import Server from './Server.vue';


  export default {
        data: function() {
            return {
              servers: [
                  { id: 1, status: 'Normal'},
                  { id: 2, status: 'Critical'},
                  { id: 3, status: 'Unknown'},
                  { id: 4, status: 'Hazardous'}
              ],
            };
        },
        components: {
            appServer: Server
        }
    }


</script>
<style scoped>
div {
border-right: 2px solid rgb(105, 105, 105);
}

.app-server {
    color: blue;
}

</style>
