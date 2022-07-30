<template>
  <div class="wrapper">
    <h2 @click="saludar">
      Hola, {{ name.toUpperCase() }} {{ surname.toUpperCase() }}
    </h2>
    <button @click="suma">+</button>
    <button @click="resta">-</button>
    <p>El número es {{ number }}</p>
    <a target="_blank" :href="link">Dragonball Multiverse</a>
    <div>
      <input v-model="message" placeholder="escribe" />
      <p>El mensaje es: {{ message }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
      name: "Javier",
      surname: "Loba",
      link: "https://www.dragonball-multiverse.com/es/read.html",
      message: "",
    };
  },
  methods: {
    saludar() {
      console.log(this.name, this.surname);
    },
    suma() {
      this.number++;
    },
    resta() {
      this.number--;
    },
  },
};
</script>

<style>
.wrapper {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 100vw;
}
div {
  margin-top: 20px;
}
</style>
