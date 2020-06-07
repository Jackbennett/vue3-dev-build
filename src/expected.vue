<template>
  <div v-if="view === 'A'" class="border" :class="css">
    <p class="grey">(grey) multi root binded <code>:class="css"</code></p>
  </div>
  <div v-if="view === 'B'" class="border" :class="css">
    <p class="blue">(blue) multi root binded <code>:class="css"</code></p>
  </div>
  <div v-if="view === 'C'" class="border" :class="css">
    <p class="red">(red) multi root binded <code>:class="css"</code></p>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  props: {
    class: String,
    type: String,
  },
  setup(props) {
    const css = ref(props.class);
    const view = ref(props.type);
    return {
      css,
      view,
    };
  },
};
</script>

<style></style>
