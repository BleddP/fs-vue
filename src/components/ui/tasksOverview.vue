<template>
  <div>
    <h2 ref="heading">Tasks</h2>
    <TaskFilter :buttonText="'Filter me'" @applyFilter="applyFilter" />
    <ul>
      <TaskItem v-for="task in list" :key="task.id" :task="task" />
    </ul>
  </div>
</template>

<script>
import TaskItem from "./TaskItem.vue";
import TaskFilter from "./TaskFilter.vue";
import tasks from "../../data/tasks";

export default {
  name: "TasksOverview",
  components: {
    TaskItem,
    TaskFilter,
  },
  data() {
    return {
      list: tasks,
    };
  },
  methods: {
    applyFilter(inputVal) {
        const filtered = tasks.filter(item => item.title.toLowerCase().includes(inputVal.toLowerCase()))
        this.list = filtered

        const headingRef = this.$refs.heading
        headingRef.style.color = 'red'
    }
  },
  watch: {
    list: function(newVal, oldVal) {
        console.log({
            newVal, oldVal
        })
    }
  },
  created() {
    console.log('component has mounted')
  }
};
</script>

<style>
</style>