<template>
  <div class="encourage-tito">
    <h1>{{ message }}</h1>
    <button @click="encourageTito">Vamos Tito!</button>
  </div>
</template>

<script lang="ts">
export default {
  name: "EncourageTito",
  data() {
    return {
      message: "Tito, você consegue dropar na rampa!",
      messages: [
        "Tito, você consegue dropar na rampa!",
        "Vai Tito, você é o melhor!",
        "Não desista Tito, você é incrível!",
        "Acredite em você, Tito!",
        "Vamos Tito, você está quase lá!",
      ],
    };
  },
  methods: {
    encourageTito() {
      const randomIndex = Math.floor(Math.random() * this.messages.length);
      this.message = this.messages[randomIndex];
    },
  },
};
</script>

<style scoped>
.encourage-tito {
  text-align: center;
  margin-top: 50px;
}

h1 {
  font-size: 2em;
  color: #2c3e50;
  margin-bottom: 20px;
}

button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 1em;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #38a169;
}
</style>
