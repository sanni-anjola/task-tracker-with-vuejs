<template>
  <header>
    <h1>{{title}}</h1>
     <Button @btn-click="$emit('toggle-add-task')" :color="showAddTask ? 'red' : 'green'" :text="showAddTask ? 'Close' : 'Add Task'"/>
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  components: {
      Button,
  },
  props: {
      title: {
          type: String,
          default: "Hello world!",
      },
      showAddTask: Boolean,
    },
    emits: ['toggle-add-task'],
};
</script>

<style scoped>
    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    }
</style>