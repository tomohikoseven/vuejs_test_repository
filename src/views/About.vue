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
    <button v-on:click="reverseMessage">Reverse Message</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "About",
  data: () => {
    return {
      counter: 0,
      message: "You loaded this page on " + new Date().toLocaleString(),
    };
  },
  methods: {
    reverseMessage() {
      this.message = this.message.split(" ").reverse().join(" ");
    },
  },
});
</script>
