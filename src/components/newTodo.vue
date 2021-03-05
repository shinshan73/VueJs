<template>
    <form action="">
        <div class="tache">
             <input v-on:type="task" id="text" placeholder="Nouvelle tâche..." required>
        </div>

          <div class="boutton">
             <input type="submit" value="+">
         </div>

          <p>
           
         </p>
    </form>
</template>

<script>

    
    export default {
    name: 'newTodo',
        methods:{
           
            
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
    }


    form{
        display: flex;
        justify-content: center;
        margin-top: 100px;
    }

    .boutton input{
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
