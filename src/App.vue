<template>
  <div>
      <h1>Vue app</h1>
      <Hello title="hello" />
  </div>
</template>

<script>
import Hello from './components/Hello.vue'

export default {
  name: 'App',
  components: {
    Hello
  }
}
</script>

<style>

</style>