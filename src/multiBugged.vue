<template>
  <div v-if="type === 'A'" class="border">
    <p class="grey">(grey) multi-root no css bind</p>
  </div>
  <div v-if="type === 'B'" class="border">
    <p class="blue">(blue) multi-root no css bind</p>
  </div>
  <div v-if="type === 'C'" class="border">
    <p class="red">(red) multi-root no css bind</p>
  </div>
</template>

<script>
export default {
  props: {
    type: String,
  },
  setup(props) {
    const type = props.type;
    return {
      type,
    };
  },
};
</script>

<style></style>
