<template>
    <div v-for="(task, index) in containTask" :key="(task, index)" class="liste">
        <input type="checkbox">
        <div class="reponse">
           {{task.description}}
        </div>
        <button class="delete is-large"></button>
    </div>
</template>

<script>
export default {
    name: 'todoList',
    props:['containTask']
}
</script>


<style scoped>

    input{
        height: 40px;
        width: 40px;
        border-radius: 100px;
    }



    .liste{
        display: flex;
        justify-content: space-between;
    }

    .reponse{
        color: white;
        font-size: 30px;
    }


</style>