<template>
  <section>
    <Ifelse class="grey append-class" type="A" />
    <Ifelse class="blue" />
    <Ifelse class="blue" />

    <Multibugged class="grey" type="A" />
    <Multibugged class="blue append-class" type="B" />
    <Multibugged class="red" type="C" />

    <Expected class="grey" type="A" />
    <Expected class="blue" type="B" />
    <Expected class="red append-class" type="C" />
  </section>
</template>

<script>
import Ifelse from "./ifelse.vue";
import Expected from "./expected.vue";
import Multibugged from "./multibugged.vue";

export default {
  components: {
    Ifelse,
    Expected,
    Multibugged,
  },
};
</script>

<style>
section {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  grid-template-rows: repeat(3, minmax(0, 1fr));
  grid-gap: 15px;
}
.border {
  border: 5px solid hotpink;
}
.grey {
  background: grey;
}
.red {
  background: red;
}
.blue {
  background: blue;
}
.append-class {
  background: indigo;
}
</style>
