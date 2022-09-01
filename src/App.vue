<template>
  <div>
      <h1>Vue app</h1>
      <Header :title="'Ik ben de header'" />
      <TasksOverview />
  </div>
</template>

<script>

import Header from './components/layout/Header.vue'
import TasksOverview from './components/ui/tasksOverview.vue'

export default {
  name: 'App',
  components: {
    Header,
    TasksOverview,
  }
}
</script>

<style>

</style>