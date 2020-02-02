<template>
    <div class="Myth-Item" v-bind:class="{'is-complete':myth.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{myth.title}}
            <button @click="$emit('del-myth', myth.id)" class="del">x</button>
        </p>
    </div>
</template>

<script>
    export default {
        name: "MythItem",
        props: ["myth"],
        methods: {
            markComplete(){
                this.myth.completed = !this.myth.completed;
            }
        }
    }
</script>

<style scoped>
    .Myth-Item{
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px dotted #ccc;
    }

    .is-complete{
        text-decoration: line-through;
    }

    .del{
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>