<template>
    <div id="app">
      <todoCard>

      </todoCard>
    </div>

        <div class="hero-foot">
        <div class="container">
          <div class="content has-text-centered pb-5">
            <p>
              <strong>Atelier Mars 2021</strong>
            </p>
            <p>
              Découvrez comment styliser simplement votre ToDo list avec 
              <a class="has-text-primary" href="https://bulma.io/">
                <strong>Bulma</strong>
              </a> 
            </p>
          </div>
        </div>
      </div>
</template>

<script>
import todoCard from './components/todoCard'

export default {
  name: 'app',
  components: {
  todoCard
  }
}
</script>


<style scoped>

</style>