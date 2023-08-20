<script>

import { defineComponent } from 'vue';
import ParentComponent from './components/ParentComponent.vue';

export default defineComponent({
  components: {
    ParentComponent,
  },
});


</script>

<template>

<div class="min-vh-100 d-flex align-items-center justify-content-center bg-light">
    <ParentComponent />
  </div>



</template>

<style scoped>

</style>
