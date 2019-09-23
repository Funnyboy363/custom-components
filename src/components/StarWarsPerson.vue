<template>
   <v-card>
       <v-card-title>
<div>
    <h3>{{ person.name }}</h3>
</div>
<div>
    {{ person.gender | allCaps }}
</div>

<span>{{ person.height }}</span>
       </v-card-title>
       <v-card-actions>
<v-button>Choose</v-button>
       </v-card-actions>
   </v-card>
</template>





<script>
export default {
    props: ["person"],
    filters: {
        allCaps(value) {
            return value.toUpperCase()
        }
    }
}
</script>





<style scoped>

</style>