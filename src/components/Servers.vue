<template>
    <div>
        <ul class="list-group">
             <li class="list-group-item" v-for="index in 5"
              v-bind:key="index.server"> Server #{{ index }} </li>
        </ul>
    </div>
</template>

<script>
</script>

<style scoped>
    div {
        border-right: 2px solid rgb(105, 105, 105);
    }
</style>
