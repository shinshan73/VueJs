<template>
    <div v-for="(task, index) in carrot" :key="(task, index)" class="liste">
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
    props:['carrot']
}
</script>

<style scoped>

    input{
        height: 25px;
        width: 25px;
        margin-right: 200px;
    }


    button{
        margin-left: 200px;
    }

    .liste{
        display: flex;
        justify-content: center;
    }


</style>