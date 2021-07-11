<template>
  <div id="about" class="about">
    <h1>This is an about page</h1>
  </div>
  <div>Counter: {{ counter }}</div>
  <div id="bind-attribute">
    <span :title="message">
      Hover your mouse over me for a few seconds to see my dynamically boud
      title!
    </span>
  </div>
  <div>
    <p>{{ message }}</p>
    <input v-model="message" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "About",
  data: () => {
    return {
      counter: 0,
      message: "Hello Vue",
    };
  },
});
</script>
