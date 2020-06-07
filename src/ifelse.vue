<template>
  <div v-if="type === 'A'" class="border" id="if-else">
    <p class="grey">(grey) if-else blocks</p>
  </div>
  <div v-else class="border" id="if-else">
    <p class="blue">(blue) if-else blocks</p>
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
