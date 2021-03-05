<template>
    <div>
    <input v-model="message" type="text" placeholder="Nouvelle tâche...">
    <button @click="emitCustomEvent"></button>
    </div>

</template>

<script>
export default {
    name: 'NewTodo',
    date(){
        return {
            message : ''
        }
    },
    methods: {
        emitCustomEvent() {
            this.$emit('custom-event-name', { value: this.message})
        }
    },
    computed :{
        /*sendTask : function(){
            const newTask = this.message
        }*/
    }
}
</script>

<style scoped>
    div {
        display: flex;
        justify-content: center;
        background-color: violet;
        
    }
    input {
        outline-style: none;
        
    }


</style>