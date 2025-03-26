<template>
  <div class="container">
    <div class="save-the-date">
      SAVE THE DATE: 28/03/2025 SERÁ O DIA EM QUE TITO DROPARÁ
    </div>
    <div class="encourage-tito">
      <h1>{{ message }}</h1>
      <button @click="encourageTito">Vamos Tito!</button>
    </div>
    <div class="additional-info">
      <h2>Informações Adicionais</h2>
      <ul>
        <li>Local: Sukata skate park</li>
        <li>Horário: 6 AM</li>
        <li>Evento: Batalha de Skate, Tito vs ele mesmo</li>
        <li>Participantes: Tito e outros skatistas incríveis</li>
        <li>Premiação: Troféu de Ouro Imaginário</li>
      </ul>
    </div>
    <div class="fun-facts">
      <h2>Curiosidades</h2>
      <p>Você sabia que Tito começou a andar de skate aos 5 anos?</p>
      <p>Tito já ganhou 10 campeonatos regionais!</p>
      <p>O movimento favorito de Tito é o kickflip.</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const messages = [
  "Tito, você consegue dropar na rampa!",
  "Vai Tito, você é o melhor!",
  "Não desista Tito, você é incrível!",
  "Acredite em você, Tito!",
  "Vamos Tito, você está quase lá!",
  "Tito, o mundo está esperando por você!",
  "Você é uma lenda, Tito!",
  "Tito, você nasceu para isso!",
  "Nada pode te parar, Tito!",
  "Tito, você é invencível!",
  "Tito, você é um campeão!",
  "Tito, você é um herói!",
  "Tito, você é uma inspiração!",
  "Tito, você é imbatível!",
  "Tito, você é fenomenal!",
];

const message = ref(messages[0]);

function encourageTito() {
  const randomIndex = Math.floor(Math.random() * messages.length);
  message.value = messages[randomIndex];
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.save-the-date {
  font-size: 2em;
  color: #e74c3c;
  text-align: center;
  font-weight: bold;
  animation: flash 1.5s infinite;
}

.encourage-tito {
  text-align: center;
  animation: pulse 2s infinite;
}

h1 {
  font-size: 3em;
  color: #8e44ad;
  margin-bottom: 20px;
  text-shadow: 2px 2px #f39c12;
  animation: bounce 1.5s infinite;
}

button {
  background-color: #e74c3c;
  color: white;
  border: none;
  padding: 15px 30px;
  font-size: 1.5em;
  cursor: pointer;
  border-radius: 10px;
  transition: background-color 0.3s, transform 0.3s;
  animation: shake 0.5s infinite;
}

button:hover {
  background-color: #c0392b;
  transform: scale(1.1);
}

.additional-info,
.fun-facts {
  color: black;
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 80%;
  text-align: left;
}

.additional-info h2,
.fun-facts h2 {
  color: #3498db;
  margin-bottom: 10px;
}

.additional-info ul {
  list-style-type: none;
  padding: 0;
}

.additional-info li,
.fun-facts p {
  font-size: 1.2em;
  margin: 5px 0;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes flash {
  0%,
  50%,
  100% {
    opacity: 1;
  }
  25%,
  75% {
    opacity: 0.5;
  }
}

@keyframes bounce {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes shake {
  0%,
  100% {
    transform: translateX(0);
  }
  25%,
  75% {
    transform: translateX(-5px);
  }
  50% {
    transform: translateX(5px);
  }
}
</style>
