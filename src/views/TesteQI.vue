<template>
    <div id="main-quiz-content">
      <h1>Quiz</h1>
      <div v-if="currentQuestion < questions.length">
        <h2>{{ questions[currentQuestion].question }}</h2>
        <ul>
          <li class="main-quiz-list " v-for="(answer, index) in questions[currentQuestion].answers" :key="index">
            <input type="radio" :id="'answer'+index" :value="answer" v-model="selectedAnswer" required>
            <label :for="'answer'+index">{{ answer }}</label>
          </li>
        </ul>
        <button @click="checkAnswer" class="main-quiz-buttons ">Submit</button>
      </div>
      <div v-else>
        <h2>Quiz Results</h2>
        <p>You answered {{ correctAnswers }} out of {{ questions.length }} questions correctly.</p>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        questions: [
          {
            question: "Quantos números ímpares existem entre 1 e 50 ?",
            answers: ["23", "24","25", "26", "27"],
            correctAnswer: "25"
          },
          {
            question: "Se você tiver 3 laranjas e der 2 para um amigo, quantas laranjas você terá ?",
            answers: ["0", "1", "2", "3", "4"],
            correctAnswer: "1"
          },
          {
            question: "Qual número deve vir em vez do ponto de interrogação? 7, 10, 8, 11, ?, 12",
            answers: ["8", "8", "10", "11", "12"],
            correctAnswer: "9"
          },
          {
            question: "Se um carro percorre 100 km com 10 litros de gasolina, quantos litros serão necessários para percorrer 250 km ?",
            answers: ["20 litros", "22,5 litros", "25 litros", "27,5 litros", "30 litros"],
            correctAnswer: "25 litros"
          },
          {
            question: "Se duas pessoas começam a correr juntas, mas uma delas corre 3 vezes mais rápido do que a outra, quanto tempo levará para que a pessoa mais rápida alcance a outra, se a pessoa mais lenta percorreu 300 metros ?",
            answers: ["50 segundos", "75 segundos", "100 segundos", "125 segundos", "150 segundos"],
            correctAnswer: "25 litros"
          },
          {
            question: "Se um carro percorre 100 km com 10 litros de gasolina, quantos litros serão necessários para percorrer 250 km ?",
            answers: ["20 litros", "22,5 litros", "25 litros", "27,5 litros", "30 litros"],
            correctAnswer: "25 litros"
          }
        ],
        currentQuestion: 0,
        selectedAnswer: null,
        correctAnswers: 0
      }
    },
    methods: {
      checkAnswer() {
        if (this.selectedAnswer === this.questions[this.currentQuestion].correctAnswer) {
          this.correctAnswers++
        }
        this.currentQuestion++
        this.selectedAnswer = null
      }
    }
  }
</script>

<style scoped>
  #main-quiz-content {
    margin: 120px 220px;
  }
  
  .main-quiz-list {
    list-style: none;
    font-size: 20px;
  }

  .main-quiz-buttons {
    margin-left: 100px;
    background: black;
    color: white;
    border: none;
    padding: 10px 50px;
    cursor: pointer;
  }

  .main-quiz-buttons:hover {
    margin-top: 5px;
    transition-duration: 0.4s;
    box-shadow: 3px 3px 5px white;
  }

  input[type=radio] {
    border: 2px solid gray;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    padding: 0;
    margin: 0 10px 0 0;
  }

  input[type=radio], label {
    cursor: pointer;
  }
</style>
  