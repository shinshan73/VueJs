<template>  
  <div>
    <header>
       <p>{{date}}</p>
       <h1>{{title}}</h1>
       <p>{{task}}Tâches</p>
    </header>
    <newTodo @custom-event-name="setMessage"/>
  </div>
</template>

<script>

  export default {
  name: 'todoCard',
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
    addTask(task){
      this.tasks.push(task);
    }
  },

}

  import newTodo from './newTodo.vue'
  export default{
    components : { newTodo},
    data(){
      return{
        message: "Hi"
      }
    },

    methods:{
      setMessage(payload){
        this.message = payload.message
      }
    }
  }
</script>

<style scoped>

div{
  background-color: #FFD700;
  height: 400px;
  width: 1000px;
  margin: 0 auto;
  margin-top: 50px;
  margin-bottom: 200px;
}

header{
  display:flex;
  justify-content: space-around;
  font-size: 25px;
}

h1{
  color: red;
}


</style>