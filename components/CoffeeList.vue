<template>
  <h1>Hola soy el componente coffee list</h1>
  <Button/>
  <!-- <ul>
    <li>{{ cafes[0].name +", "+cafes[0].country }}</li>
    <li>{{ cafes[1].name +", "+ cafes[1].country }}</li>
  </ul> -->
</template>

<script>
import Button from './Button.vue';
export default {
  name: "CoffeeList",
  components: { Button },
  data() {
    return {
      cafes: [
        { name: "cafe 1", country: "Brasil" },
        { name: "cafe2", country: "Colombia" },
      ],
    };
  },
};
</script>

<style></style>
