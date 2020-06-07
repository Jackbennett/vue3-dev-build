<template>
  <div v-if="view === 'A'" class="border">
    <p class="grey">(grey) multi-root no css bind</p>
  </div>
  <div v-if="view === 'B'" class="border">
    <p class="blue">(blue) multi-root no css bind</p>
  </div>
  <div v-if="view === 'C'" class="border">
    <p class="red">(red) multi-root no css bind</p>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  props: {
    type: String,
  },
  setup(props) {
    const view = ref(props.type);
    return {
      view,
    };
  },
};
</script>

<style></style>
