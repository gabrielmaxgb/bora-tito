<template>
  <div class="container">
    <div class="save-the-date">
      SAVE THE DATE: 28/03/2025 SERÁ O DIA EM QUE TITO E VITU DROPARÃO
    </div>
    <div class="encourage-tito">
      <h1>{{ message }}</h1>
      <button @click="encourageTito">Vamos Tito E Vitu!</button>
    </div>
    <div class="additional-info">
      <h2>Informações Adicionais</h2>
      <ul>
        <li>Local: Sukata skate park</li>
        <li>Horário: 6 AM</li>
        <li>Evento: Batalha de Skate, Tito e Vitu vs eles mesmos</li>
        <li>Participantes: Tito, Vitu e outros skatistas incríveis</li>
        <li>Premiação: Troféu de Ouro Imaginário</li>
      </ul>
    </div>
    <div class="fun-facts">
      <h2>Curiosidades</h2>
      <p>Você sabia que Tito/Vitu começou a andar de skate aos 5 anos?</p>
      <p>Tito/Vitu já ganhou 10 campeonatos regionais!</p>
      <p>O movimento favorito de Tito/Vitu é o kickflip.</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const messages = [
  "Tito e Vitu, vocês conseguem dropar na rampa!",
  "Vai Tito e Vitu, vocês são os melhores!",
  "Não desistam Tito e Vitu, vocês são incríveis!",
  "Acreditem em vocês, Tito e Vitu!",
  "Vamos Tito e Vitu, vocês estão quase lá!",
  "Tito e Vitu, o mundo está esperando por vocês!",
  "Vocês são uma lenda, Tito e Vitu!",
  "Tito e Vitu, vocês nasceram para isso!",
  "Nada pode parar vocês, Tito e Vitu!",
  "Tito e Vitu, vocês são invencíveis!",
  "Tito e Vitu, vocês são campeões!",
  "Tito e Vitu, vocês são heróis!",
  "Tito e Vitu, vocês são uma inspiração!",
  "Tito e Vitu, vocês são imbatíveis!",
  "Tito e Vitu, vocês são fenomenais!",
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
  /* animation: pulse 2s infinite; */
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
