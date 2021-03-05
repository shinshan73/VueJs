<template>  
  <div>
    <header>
       <p>{{date}}</p>
       <h1>{{title}}</h1>
       <p>{{tasks.length}} Tâches</p>
    </header>
    <newTodo v-on:addTask="submitTask">
    </newTodo>
    <todoList v-bind:carrot="tasks"></todoList>
  </div>

</template>

<script>
import newTodo from './newTodo'
import todoList from './todoList';

  export default {
  name:'todoCard',
  components:{
    newTodo,
    todoList
  },
  data() {

      return {
        day: ["Lundi","Mardi", "Mercredi", "Jeudi","Vendredi","Samedi","Dimanche"],
        month: ["Janvier", "Février", "Mars"," Avril","Mai","Juin","Juillet","Aout","Septembre","Octobre","Novembre","Décembre"],
        tasks: [],
        title: "VueJs Tutorial ToDo List",
      }
  },
  
  computed: {
    date: function() {
     let today = new Date();
     let todate = `${this.day[(today.getDay()-1)]}` + ' ' + today.getDay() + '-' + `${this.month[(today.getMonth())]}`;
      return todate; 
    }
  },

   methods:{
      submitTask(task){
        this.tasks.push({
          description: task, done: false
        });
      }
    }, 


}

  
   
</script>

<style scoped>

div{
  background-color: #FFD700;
  width: 1000px;
  margin: 0 auto;
  margin-top: 50px;
  padding-bottom: 50px;
}

header{
  display:flex;
  justify-content: space-around;
  font-size: 25px;
}

h1{
  color: red;
}

.liste{
  margin-top: 100px;
}



</style>