<script>
import NewTodo from './NewTodo'
import TodoList from './TodoList'
export default {
    
    name : 'TodoCard',
    data() {
        return {
            tasks: [],
            message: ''
            
        }
    },

    computed:{
        date: function(){
                    const now = new Date()
                    const day = now.toLocaleString("default", { weekday : "long"})
                    const month = now.toLocaleString("default", {month: "long"})
                    return `${day} ${now.getDay()} ${month}`
                }
    },
    components: { NewTodo, TodoList },
    methods: {
        setMessage(message) {
            if (message === ''){
                console.log('vide')
            }else{
            this.tasks.push({msg: message.value, done: false})
            console.log(this.tasks)
            }
        }
    }
    
  
} 

</script>


<template>
    <div id="back">
        <div id="card">

        
       <nav id="navCard"> <p>{{ date }}</p>
       <h1>VueJs Tutorial ToDo List </h1>
        <p>{{tasks.length}} tâche(s)</p>
        </nav> 
        
        <NewTodo @custom-event-name= "setMessage" />  

        <TodoList v-bind:export="tasks"/>

        </div> 
    </div>
</template>




<style scoped>
#card {
    background-color: white;
    margin: 0 100px 0 100px;
}
#back {
    border: solid 1px black;
    width: 100vw;
    height: 100vh;
}
#navCard {   
    display: flex;
    justify-content: space-between;
    background-color: white;
    margin: 100px 0px 10px 0px;
    
    
}

</style>
