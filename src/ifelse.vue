<template>
  <div v-if="view === 'A'" class="border" id="if-else">
    <p class="grey">(grey) if-else blocks</p>
  </div>
  <div v-else class="border" id="if-else">
    <p class="blue">(blue) if-else blocks</p>
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
