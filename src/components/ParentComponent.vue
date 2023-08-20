
<script>
import { defineComponent, ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

export default defineComponent({
  components: {
    ChildComponent,
  },
  setup() {
    const message = ref('Hello from Parent');
    const receivedMessage = ref('');

    const handleMessageEmitted = (msg) => {
      receivedMessage.value = msg;
    };

    return {
      message,
      receivedMessage,
      handleMessageEmitted,
    };
  },
});
</script>





<template>
    <div class="container mt-5">
      <h1 class="mb-4">Parent Component</h1>
      <p>Message from Child Component: {{ receivedMessage }}</p>
      <ChildComponent :message="message" @messageEmitted="handleMessageEmitted" />
    </div>
</template>