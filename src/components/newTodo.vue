<template>
    <form action="">
        <div class="tache">
             <input v-model="task" type="text" id="task" placeholder="Nouvelle tâche..." required>
        </div>

          <div class="boutton">
            <button v-on:click="message">+</button>
         </div>            
    </form>
    <todoList>
    </todoList>
</template>

<script>

    import todoList from './todoList'

    export default {
    name: 'newTodo',
    components:{
        todoList,
    },
    data(){
        return {
            task:''
        }
    },

        methods:{
         message() {
             this.$emit('addTask',this.task)
         }
    },

        
    }

</script>

<style scoped>

   .tache input{
        border: none;
        height: 100px;
        width: 350px;
        text-align: center;
        font-size: 20px;
        border-radius: 20px;
    }


    form{
        display: flex;
        justify-content: center;
        margin-top: 100px;
    }

    button{
        width: 60px;
        height: 60px;
        border-radius: 30px;
        background: green;  
        margin-top: 15px;
        margin-left: 20px;
        font-size: 50px;
        color: white;
        font-family: sans-serif;
        border: none;
    }

    input{
        font-family: none;
    }

    
    

</style>
