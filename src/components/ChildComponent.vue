<script>
import { defineComponent, ref, defineEmits } from 'vue';

export default defineComponent({
  props: {
    message: String,
  },
  setup(props) {
    const emit = defineEmits();
    
    const emitMessage = () => {
      const customMessage = 'Custom message from Child';
      emit('messageEmitted', customMessage);
    };

    return {
      emitMessage,
    };
  },
});
</script>

<template>
    <div class="card p-4">
      <h2 class="card-title">Child Component</h2>
      <p>Received message from Parent: {{ message }}</p>
      <button class="btn btn-primary" @click="emitMessage">Emit Message</button>
    </div>
  </template>