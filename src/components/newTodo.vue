<template>
    <button @click="emitCustomEvent">Emit Event</button>
</template>


<script>
export default {
   methods:{
       emitCustomEvent() {
           this.$emit('custom-event-name', {message: 'My custom message'})
       }
   }
}
</script>