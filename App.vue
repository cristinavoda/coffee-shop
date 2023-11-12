<template>
  <h1>{{ coffees[count].name}}</h1>
  <h2>{{ coffees[count].info }}</h2>
  <img :src=' coffees[count].image '/>
  <p>{{ count }}</p>
  <Button @click="changeCoffee"/>

  <form>
    <label>Name:</label>
    <input v-model="name" />
    <label>info:</label>
    <input v-model="info" />
    <label>image:</label>
    <input v-model="image" />
    <Button @click.prevent="addCoffee"/>
  </form>
  <h1>{{ name }}</h1>
  <h2>{{ info }}</h2>
  
</template>

<script>
import Button from "./components/Button.vue";
export default {
  name: "App",
  components: { Button },
  data() {
    return {
      coffees: [
        {
          name: "Expresso",
          info: "café solo",
          image: "../public/img/expreso.png",
        },
        {
          name: "Americano",
          info: "café rebajado",
          image: "../public/img/americano.png",
        },
        {
          name: "Macchiato",
          info: "espumoso",
          image: "../public/img/macchiato.png",
        },
        {
          name: "Cortado",
          info: "poquita leche, mucho café.",
          image: "../public/img/cortado.png",
        },
        {
          name: "Café con leche",
          info: "mitad leche, mitad café",
          image: "../public/img/café con leche.png",
        },
        {
          name: "Café lágrima",
          info: "lo contrario al cortado",
          image: "../public/img/lágrima.png",
        },
        {
          name: "Capuchino",
          info: "bien de espuma y leche con topping de cacao y canela",
          image: "../public/img/cappuchino.png",
        },
        {
          name: "Café Latte",
          info: "con leche cremosa",
          image: "../public/img/café latte.png",
        },
        {
          name: "Irlandés",
          info: "con un poquito de whisky y nata",
          image: "../public/img/irlandés.png",
        },
        {
          name: "Café hawaiano",
          info: "con leche de coco",
          image: "../public/img/hawaiano.png",
        },
        {
          name: "Café árabe",
          info: "con especias",
          image: "../public/img/árabe.png",
        },
      ],
      count: 0,
      show: false,
      name: "",
      info: "",
      image: "",
    };
  },
  methods: {

    changeCoffee() {
      if (this.count === this.coffees.length - 1 ) {
        this.count = 0;
      }

      return this.count++;
    },
    addCoffee() {

      return this.coffees.push({
        name: this.name,
        info: this.info,
        image: this.image,
      });
    },
  },
};
</script>

<style>
/*css*/
.h1 {
  color: brown;
}

* {
  margin: 0;
  text-align: center;
}

a {
  color: rgb(99, 98, 98);
  text-decoration: none;
}
.active {
  color: blue;
  text-decoration: underline;
}
</style>
