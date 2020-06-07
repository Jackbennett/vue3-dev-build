<template>
  <div v-if="type === 'A'" class="border" :class="css">
    <p class="grey">(grey) multi root binded <code>:class="css"</code></p>
  </div>
  <div v-if="type === 'B'" class="border" :class="css">
    <p class="blue">(blue) multi root binded <code>:class="css"</code></p>
  </div>
  <div v-if="type === 'C'" class="border" :class="css">
    <p class="red">(red) multi root binded <code>:class="css"</code></p>
  </div>
</template>

<script>
export default {
  props: {
    class: String,
    type: String,
  },
  setup(props) {
    const css = props.class;
    const type = props.type;
    return {
      css,
      type,
    };
  },
};
</script>

<style></style>
