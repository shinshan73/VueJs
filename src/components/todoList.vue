<template>
    <form action="">
        <label class="checkbox">
        <input type="checkbox">
            <p>
                {{task}}
            </p>    
        </label>
        <button class="delete is-large"></button>
    </form>
</template>

<script>
export default {
    name: 'todoList',
    props:['task']
}
</script>

<style scoped>

    input{
        height: 25px;
        width: 25px;
        margin-right: 100px;
    }

    form{
        display: flex;
        justify-content: center;
    }

    button{
        margin-left: 100px;
    }

</style>