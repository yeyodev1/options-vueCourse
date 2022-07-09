<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
  <button ref="btn">Click!</button>
</template>

<script setup>
import {
  defineExpose,
  defineProps,
  watch,
  ref,
  toRefs,
  computed,
  inject,
} from "vue";

const props = defineProps({
  name: String,
  lastName: String,
});

const { name, lastName } = toRefs(props);

const fullName = computed(() => {
  return `${name.value} ${lastName.value}`;
});

const username = inject("username");

defineExpose({
  fullName,
});

const btn = ref(null);

console.log(btn.value);

watch(btn, (valor) => {
  console.log(valor);
});
</script>
