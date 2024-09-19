<template>
  <li
    class="list-group-item d-flex align-items-center justify-content-between mb-2"
    :class="completedClass"
    style="background-color: #f4f6f7;"
  >
    <div>
      <input type="checkbox" v-model="task.completed" class="form-check-input me-2" />
      <span v-if="task.completed" class="text-decoration-line-through">{{ task.text }}</span>
      <span v-else>{{ task.text }}</span>
    </div>
    <div>
      <a href="#!" class="text-info" title="Sửa công việc"><i class="fas fa-pencil-alt me-3"></i></a>
      <a href="#!" class="text-danger" title="Xóa công việc"><i class="fas fa-trash-alt"></i></a>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    task: Object,
  },
  computed: {
    completedClass() {
      return this.task.completed ? 'border-0' : '';
    },
  },
};
</script>
