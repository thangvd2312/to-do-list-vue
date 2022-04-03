<template>
  <div id="app">
    <Task :tasks="tasks" @update-tasks="updateTask" />
  </div>
</template>

<script>
import Task from "./components/Task";

export default {
  name: "App",
  components: {
    Task,
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Learn Vue JS",
          completed: false,
        },
        {
          id: 2,
          title: "Watch netflix",
          completed: false,
        },
        {
          id: 3,
          title: "Go shopping",
          completed: false,
        },
        {
          id: 4,
          title: "Learn guitar",
          completed: false,
        },
        {
          id: 5,
          title: "Send email",
          completed: false,
        },
      ],
    };
  },
  methods: {
    updateTask(payload) {
      this.tasks = payload;
    },
  },
};
</script>

