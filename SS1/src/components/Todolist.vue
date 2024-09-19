<template>
  <ul class="list-group mb-0">
    <TodoItem
      v-for="(item, index) in tasks"
      :key="index"
      :task="item"
    />
  </ul>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
  components: {
    TodoItem,
  },
  data() {
    return {
      tasks: [
        { text: 'Cras justo odio', completed: true },
        { text: 'Cras justo odio', completed: false },
      ],
    };
  },
};
</script>
