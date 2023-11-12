<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
  name: "Button",
  data() {
    return {
      text: "Show!",
    };
  },
};
</script>

<style>
button {
  background-color: rgb(6, 125, 86);
  border-radius: 0.2rem;
  border: 0;
  padding: 0.2rem 1rem 0.2rem 1rem;
  color: rgb(255, 255, 255);
}
button:hover  {
  background-color: rgb(17, 206, 143);
}
</style>
