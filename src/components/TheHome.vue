<template>
  <div>{{ fullName }}</div>
</template>

<script>
import { toRefs, computed } from "vue";

export default {
  props: {
    name: String,
    lastName: String,
  },

  setup(props) {
    const { name, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${name.value} ${lastName.value}`;
    });

    return {
      fullName,
    };
  },
};
</script>
