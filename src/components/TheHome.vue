<template>
  <div>{{ fullName }}</div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  setup() {
    const name = ref("Diego");
    const lastName = ref("Reyes");

    const fullName = computed(() => {
      return `${name.value} ${lastName.value}`;
    });

    return {
      fullName,
    };
  },
};
</script>
