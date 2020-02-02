<template>
    <div>
        <div v-bind:key="myth.id" v-for="myth in myths">
            <MythItem v-bind:myth="myth" v-on:del-myth="$emit('del-myth', myth.id)"/>
        </div>
    </div>
</template>

<script>
    import MythItem from "./MythItem";

    export default {
        name: "Myths",
        components: {
            MythItem
        },
        props: ["myths"]
    }
</script>

<style scoped>

</style>