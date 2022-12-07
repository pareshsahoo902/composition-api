<template>
  <course-goals></course-goals>
</template>

<script>
import CourseGoals from "./components/CourseGoals.vue";
export default {
  components: {
    CourseGoals,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  font-family: sans-serif;
}
body {
  margin: 0;
  background-color: #0d5e45;
}
.container {
  box-shadow: 0 2px 8px rgba(12, 12, 12, 0.372);
  max-width: 25rem;
  margin: 3rem auto;
  padding: 1rem;
  border-radius: 12px;
}
button {
  background-color: #155311;
  border: 1px solid #395745;
  color: white;
  border-radius: 12px;
  font: inherit;
  cursor: pointer;
  padding: 0.5rem 1.5rem;
  margin-right: 1rem;
}
button:hover,
button:active {
  background-color: #089067;
  border-color: #033538;
}
</style>