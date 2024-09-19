<template>
  <form class="d-flex justify-content-center align-items-center mb-4" @submit.prevent="addTask">
    <div class="form-outline flex-fill">
      <input v-model="newTask" type="text" id="form2" class="form-control" placeholder="Thêm công việc" />
    </div>
    <button type="submit" class="btn btn-info ms-2">Thêm</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      newTask: '',
    };
  },
  methods: {
    addTask() {
      // Emit the task to the parent or store
      console.log(this.newTask);
      this.newTask = '';
    },
  },
};
</script>
