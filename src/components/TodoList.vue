<script>
export default {
    name: 'TodoList', 
    props: {
        tasks: Array,
    }
}
</script>

<template>
    <ul>
        <li><p>Liste des tâches:</p></li>
        <li v-for="(task, index) in tasks" v-bind:key="index">
            <input type="checkbox">
            <p>{{}}</p>
            <button></button>
        </li>
    </ul>
</template>

<style scoped>

</style>