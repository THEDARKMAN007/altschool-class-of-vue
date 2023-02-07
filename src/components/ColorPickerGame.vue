<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { randomColor } from "../composables/colorPicker";
const { colors, message, matchColor } = randomColor();

export default {
  data() {
    return {
      colors: colors,
      message: message,
    };
  },
  methods: { matchColor },
};
</script>

<style>

</style>
