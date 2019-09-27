<template>
<div>
  <p v-if="!server">Please select a Server</p>
        <p v-else>Server #{{ server.id }} selected, Status: {{ server.status }}</p>
<v-btn @click="resetStatus">Change to normal </v-btn>
</div>
</template>
<script>
import { serverBus } from '../main';
export default {
        data: function() {
            return {
                server: null
            }
        },
        methods: {
          resetStatus() {
              this.server.status = 'Normal';
          }
        },
        created() {
            serverBus.$on('serverSelected', (server) => {
                this.server = server;
            });
        }
    }
</script>
<style scoped>
</style>
