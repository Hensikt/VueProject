<template>
    <div>
        <div v-for="myth in Myths">
<!--            <MythsItem v-bind:Myth="myth"/>-->
            <h3>{{myth.title}}</h3>
        </div>
    </div>
</template>

<script>
    // import MythsItem from "./MythsItem";

    export default {
        name: "Myths",
        props: ["myths"]
    }
</script>

<style scoped>

</style>