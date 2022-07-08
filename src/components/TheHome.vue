<template>
  <div>{{ fullName }}</div>
  <div>{{ username }}</div>
</template>

<script>
import { toRefs, computed, inject } from "vue";

export default {
  props: {
    name: String,
    lastName: String,
  },

  setup(props, { expose }) {
    const { name, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${name.value} ${lastName.value}`;
    });

    const username = inject("username");

    expose({
      fullName,
    });

    return {
      fullName,
      username,
    };
  },
};
</script>
