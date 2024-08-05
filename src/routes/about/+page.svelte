<!-- <script lang="ts">
    let questions = [
      {
        question: "Which of the following computer language used for artificial intelligence?",
        options: ["Python", "Java", "Prolog", "C++"],
        correctAnswer: 2
      },
      {
        question: "The different types of machine learning are?",
        options: ["Supervised", "Unsupervised", "Reinforcement", "All of the above"],
        correctAnswer: 3
      }
    ];
  
    let answers = new Array(questions.length).fill(null);
    let questionPointer = -1;
  
    function getScore() {
      let score = answers.reduce((acc, value, index) => {
        if (questions[index].correctAnswer == value) {
          return acc + 1;
        }
        return acc;
      }, 0);
      return (score / questions.length * 100) + "%";
    }
  
    function restartQuiz() {
      answers = new Array(questions.length).fill(null);
      questionPointer = -1;
    }
  
    function startQuiz() {
      questionPointer = 0;
    }
</script>
  
<style>
    body {
        margin: 0;
        font-family: 'Arial', sans-serif;
        background-color: #f0f4f8;
    }
  
    .app {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background: linear-gradient(135deg, #e0eaff, #d8d8e1);
    }
  
    .app > div {
        width: 100%;
        max-width: 600px;
        background: #fff;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        display: flex;
        flex-direction: column;
    }
  
    .start-screen,
    .score-screen,
    .quiz-screen {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 2em;
    }
  
    .start-screen img {
        max-width: 100%;
        height: auto;
        border-radius: 12px;
        margin-bottom: 20px;
    }
  
    .start-screen button,
    .score-screen button {
        padding: 12px 24px;
        font-size: 1.1em;
        background: #007bff;
        color: white;
        border: none;
        border-radius: 25px;
        cursor: pointer;
        transition: background-color 0.3s ease, transform 0.2s ease;
    }
  
    .start-screen button:hover,
    .score-screen button:hover {
        background: #0056b3;
    }
  
    .start-screen button:focus,
    .score-screen button:focus {
        outline: none;
        box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.5);
    }
  
    .quiz-screen .main {
        width: 100%;
        text-align: center;
    }
  
    .quiz-screen h2 {
        margin-bottom: 20px;
        font-size: 1.5em;
        color: #333;
    }
  
    .Options {
        display: flex;
        flex-wrap: wrap;
        gap: 15px;
        justify-content: center;
    }
  
    .Options button {
        width: 45%;
        padding: 12px;
        font-size: 1em;
        color: #333;
        background: #f8f9fa;
        border: 2px solid #ddd;
        border-radius: 25px;
        cursor: pointer;
        transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
    }
  
    .Options button.selected {
        background: #007bff;
        color: white;
        border-color: #007bff;
    }
  
    .Options button:hover {
        background: #e2e6ea;
    }
  
    .Options button:focus {
        outline: none;
        box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.5);
    }
  
    .footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 20px;
        width: 100%;
    }
  
    .progress-bar {
        width: 150px;
        height: 10px;
        background: #ddd;
        border-radius: 10px;
        overflow: hidden;
    }
  
    .progress-bar div {
        height: 100%;
        background: #007bff;
        transition: width 0.3s ease;
    }
  
    .footer .buttons button {
        padding: 10px;
        background: #007bff;
        color: white;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        font-size: 1.2em;
        transition: background-color 0.3s ease;
    }
  
    .footer .buttons button:hover {
        background: #0056b3;
    }
  
    .footer .buttons button:disabled {
        background: #b0bec5;
        cursor: not-allowed;
    }
  
    .score-screen h1 {
        margin-bottom: 20px;
        font-size: 2em;
        color: #333;
    }
</style>

<div class="app">
    {#if questionPointer === -1}
      <div class="start-screen">
        <img src="/program.jpeg" alt="cs" />
        <button on:click={startQuiz}>
          Start Quiz
        </button>
      </div>
    {:else if !(questionPointer > answers.length - 1)}
      <div class="quiz-screen">
        <div class="main">
          <h2>{questions[questionPointer].question}</h2>
          <div class="Options">
            {#each questions[questionPointer].options as opt, i}
              <button class={answers[questionPointer] == i ? 'selected' : ''} on:click={() => { answers[questionPointer] = i }}>
                {opt}
              </button>
            {/each}
          </div>
        </div>
        <div class="footer">
          <div class="progress-bar">
            <div style="width:{(questionPointer / questions.length) * 100}%"></div>
          </div>
          <div class="buttons">
            <button on:click={() => questionPointer--} disabled={questionPointer == 0}>
              &lt;
            </button>
            <button on:click={() => questionPointer++}>
              &gt;
            </button>
          </div>
        </div>
      </div>
    {:else}
      <div class="score-screen">
        <h1>Your Score: {getScore()}</h1>
        <button on:click={restartQuiz}>Restart Quiz</button>
      </div>
    {/if}
</div> -->


<!-- 

   <script lang="ts">
    let questions = [
      {
        question: "Which of the following computer language used for artificial intelligence?",
        options: ["Python", "Java", "Prolog", "C++"],
        correctAnswer: 2
      },
      {
        question: "The different types of machine learning are?",
        options: ["Supervised", "Unsupervised", "Reinforcement", "All of the above"],
        correctAnswer: 3
      }
    ];
    
    let answers = new Array(questions.length).fill(null);
    let questionPointer = -1;
  
    function getScore() {
      let score = answers.reduce((acc, value, index) => {
        if (questions[index].correctAnswer == value) {
          return acc + 1;
        }
        return acc;
      }, 0);
      return (score / questions.length * 100) + "%";
    }
  
    function restartQuiz() {
      answers = new Array(questions.length).fill(null);
      questionPointer = -1;
    }
  
    function startQuiz() {
      questionPointer = 0;
    }
</script>

<div class="absolute inset-0 flex justify-center items-center bg-gray-200">
    {#if questionPointer === -1}
      <div class="flex flex-col items-center">
        <img src="/program.jpeg" alt="cs" class="max-w-full h-auto mb-5 rounded-xl" />
        <button on:click={startQuiz} class="py-2 px-4 bg-blue-500 text-blue-100 rounded-lg shadow-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-400">
          Start Quiz
        </button>
      </div>
    {:else if !(questionPointer > answers.length - 1)}
      <div class="flex flex-col items-center">
        <div class="p-12">
          <h2 class="text-xl font-semibold mb-4">{questions[questionPointer].question}</h2>
          <div class="flex flex-wrap gap-2">
            {#each questions[questionPointer].options as opt, i}
              <button class={`w-1/2 py-2 px-4 rounded-lg ${answers[questionPointer] == i ? 'bg-gray-900 text-gray-100' : 'bg-gray-200'} border border-gray-300`} on:click={() => { answers[questionPointer] = i }}>
                {opt}
              </button>
            {/each}
          </div>
        </div>
        <div class="fixed bottom-0 left-0 w-full h-12 flex justify-between items-center bg-gray-200 p-2">
          <div class="w-36 h-2 bg-gray-300 rounded-full overflow-hidden">
            <div class="h-full bg-blue-500" style="width:{(questionPointer / questions.length) * 100}%"></div>
          </div>
          <div class="flex space-x-2">
            <button on:click={() => questionPointer--} disabled={questionPointer == 0} class="py-1 px-2 bg-gray-300 rounded-lg text-gray-600 disabled:opacity-50">
              &lt;
            </button>
            <button on:click={() => questionPointer++} class="py-1 px-2 bg-gray-300 rounded-lg text-gray-600">
              &gt;
            </button>
          </div>
        </div>
      </div>
    {:else}
      <div class="flex flex-col items-center">
        <h1 class="text-2xl font-semibold mb-4">Your Score: {getScore()}</h1>
        <button on:click={restartQuiz} class="py-2 px-4 bg-blue-500 text-white rounded-lg shadow-md hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-400">
          Restart Quiz
        </button>
      </div>
    {/if}
</div> -->


<script lang="ts">
  import { page } from '$app/stores';
  import { onMount } from 'svelte';

  let name = '';
  let age = '';
  let major = '';

  onMount(() => {
      const urlParams = new URLSearchParams(window.location.search);
      name = urlParams.get('name') || '';
      age = urlParams.get('age') || '';
      major = urlParams.get('major') || '';
  });

  let questions = [
    {
      question: "Which of the following computer language used for artificial intelligence?",
      options: ["Python", "Java", "Prolog", "C++"],
      correctAnswer: 2
    },
    {
      question: "The different types of machine learning are?",
      options: ["Supervised", "Unsupervised", "Reinforcement", "All of the above"],
      correctAnswer: 3
    }
  ];

  let answers = new Array(questions.length).fill(null);
  let questionPointer = -1;

  function getScore() {
    let score = answers.reduce((acc, value, index) => {
      if (questions[index].correctAnswer == value) {
        return acc + 1;
      }
      return acc;
    }, 0);
    return (score / questions.length * 100) + "%";
  }

  function restartQuiz() {
    answers = new Array(questions.length).fill(null);
    questionPointer = -1;
  }

  function startQuiz() {
    questionPointer = 0;
  }
</script>

<style>
  body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background-color: #f0f4f8;
  }

  .app {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background: linear-gradient(135deg, #e0eaff, #d8d8e1);
  }

  .app > div {
      width: 100%;
      max-width: 600px;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      display: flex;
      flex-direction: column;
  }

  .start-screen,
  .score-screen,
  .quiz-screen {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 2em;
  }

  .start-screen img {
      max-width: 100%;
      height: auto;
      border-radius: 12px;
      margin-bottom: 20px;
  }

  .start-screen button,
  .score-screen button {
      padding: 12px 24px;
      font-size: 1.1em;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.2s ease;
  }

  .start-screen button:hover,
  .score-screen button:hover {
      background: #0056b3;
  }

  .start-screen button:focus,
  .score-screen button:focus {
      outline: none;
      box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.5);
  }

  .user-details {
      margin-top: 20px;
      text-align: left;
  }

  .user-details p {
      margin: 5px 0;
      font-size: 1.2em;
      color: #333;
  }

  .quiz-screen .main {
      width: 100%;
      text-align: center;
  }

  .quiz-screen h2 {
      margin-bottom: 20px;
      font-size: 1.5em;
      color: #333;
  }

  .Options {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
  }

  .Options button {
      width: 45%;
      padding: 12px;
      font-size: 1em;
      color: #333;
      background: #f8f9fa;
      border: 2px solid #ddd;
      border-radius: 25px;
      cursor: pointer;
      transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
  }

  .Options button.selected {
      background: #007bff;
      color: white;
      border-color: #007bff;
  }

  .Options button:hover {
      background: #e2e6ea;
  }

  .Options button:focus {
      outline: none;
      box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.5);
  }

  .footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 20px;
      width: 100%;
  }

  .progress-bar {
      width: 150px;
      height: 10px;
      background: #ddd;
      border-radius: 10px;
      overflow: hidden;
  }

  .progress-bar div {
      height: 100%;
      background: #007bff;
      transition: width 0.3s ease;
  }

  .footer .buttons button {
      padding: 10px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      font-size: 1.2em;
      transition: background-color 0.3s ease;
  }

  .footer .buttons button:hover {
      background: #0056b3;
  }

  .footer .buttons button:disabled {
      background: #b0bec5;
      cursor: not-allowed;
  }

  .score-screen h1 {
      margin-bottom: 20px;
      font-size: 2em;
      color: #333;
  }
</style>

<div class="app">
  {#if questionPointer === -1}
    <div class="start-screen">
      <img src="/program.jpeg" alt="cs" />
      <button on:click={startQuiz}>
        Start Quiz
      </button>
      <div class="user-details">
        <p><strong>Name:</strong> {name}</p>
        <p><strong>Age:</strong> {age}</p>
        <p><strong>Major:</strong> {major}</p>
      </div>
    </div>
  {:else if !(questionPointer > answers.length - 1)}
    <div class="quiz-screen">
      <div class="main">
        <h2>{questions[questionPointer].question}</h2>
        <div class="Options">
          {#each questions[questionPointer].options as opt, i}
            <button class={answers[questionPointer] == i ? 'selected' : ''} on:click={() => { answers[questionPointer] = i }}>
              {opt}
            </button>
          {/each}
        </div>
      </div>
      <div class="footer">
        <div class="progress-bar">
          <div style="width:{(questionPointer / questions.length) * 100}%"></div>
        </div>
        <div class="buttons">
          <button on:click={() => questionPointer--} disabled={questionPointer == 0}>
            &lt;
          </button>
          <button on:click={() => questionPointer++}>
            &gt;
          </button>
        </div>
      </div>
    </div>
  {:else}
    <div class="score-screen">
      <h1>Your Score: {getScore()}</h1>
      <button on:click={restartQuiz}>Restart Quiz</button>
    </div>
  {/if}
</div>
