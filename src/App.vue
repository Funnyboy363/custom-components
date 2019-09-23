<template>
    <v-container>
        <app-header></app-header>
        <hr>
       
         <v-row>
           <v-col cols="6">
            <servers></servers></v-col>
             <v-col cols="6">
            <app-server-details></app-server-details>
             </v-col>
         </v-row>
        <hr>
        <app-footer></app-footer>
    </v-container>
</template>

<script>
    import Header from './components/Header.vue';
    import Footer from './components/Footer.vue';
    import Servers from './components/Servers.vue';
    import ServerDetails from './components/ServerDetails.vue';

    export default {
        components: {
            appHeader: Header,
            Servers,
            'app-server-details': ServerDetails,
            'app-footer': Footer
        }
    }
</script>

<style>
html, div.row, ul {
   padding-left: 10px;
}
</style>
