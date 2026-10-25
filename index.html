
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AIZONE PRINCE - Class 10 Quiz</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f1f5f9;
    }
    .option {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #cbd5e1;
      border-radius: 10px;
      text-align: left;
      background: white;
      cursor: pointer;
    }
    .option:hover {
      background: #dbeafe;
    }
    .correct {
      background: #bbf7d0;
    }
    .wrong {
      background: #fecaca;
    }
  </style>
</head>
<body class="p-4">
  <div class="max-w-xl mx-auto bg-white p-5 rounded-2xl shadow">
    <h1 class="text-2xl font-bold text-center text-blue-700">
      AIZONE PRINCE
    </h1>
    <h2 class="text-center text-lg mt-2">Class 10 Objective Test</h2>

    <div class="flex gap-2 mt-4">
      <button onclick="setLanguage('hi')"
        class="bg-blue-600 text-white p-2 rounded flex-1">
        हिंदी
      </button>
      <button onclick="setLanguage('en')"
        class="bg-green-600 text-white p-2 rounded flex-1">
        English
      </button>
    </div>

    <label class="block mt-4 font-bold" id="subjectLabel">
      विषय चुनें
    </label>
    <select id="subject" class="w-full border p-3 rounded mt-2"
      onchange="startQuiz()">
      <option value="math">गणित / Maths</option>
      <option value="science">विज्ञान / Science</option>
      <option value="sst">सामाजिक विज्ञान / SST</option>
      <option value="hindi">हिंदी / Hindi</option>
      <option value="english">अंग्रेज़ी / English</option>
    </select>

    <div class="flex justify-between mt-5">
      <span id="questionCount">प्रश्न 1</span>
      <span id="timer">समय: 10:00</span>
    </div>

    <div class="w-full bg-gray-200 rounded-full h-2 mt-2">
      <div id="progress" class="bg-blue-600 h-2 rounded-full"
        style="width:0%"></div>
    </div>

    <h3 id="question" class="font-bold text-lg mt-5">
      प्रश्न यहाँ दिखाई देगा
    </h3>

    <div id="options" class="mt-3"></div>

    <button id="nextBtn" onclick="nextQuestion()"
      class="w-full bg-blue-600 text-white p-3 rounded-xl mt-4">
      अगला प्रश्न
    </button>

    <div id="result" class="hidden mt-5 text-center">
      <h2 class="text-2xl font-bold">टेस्ट पूरा हुआ!</h2>
      <p id="score" class="text-lg mt-2"></p>
      <button onclick="startQuiz()"
        class="bg-green-600 text-white p-3 rounded-xl mt-4">
        फिर से टेस्ट दें
      </button>
    </div>
  </div>

<script>
let language = "hi";
let current = 0;
let score = 0;
let answered = false;
let timeLeft = 600;
let timerInterval;

const questions = {
  math: [
    {
      hi: "2 + 3 का मान क्या है?",
      en: "What is 2 + 3?",
      optionsHi: ["4", "5", "6", "7"],
      optionsEn: ["4", "5", "6", "7"],
      answer: 1
    },
    {
      hi: "यदि x + 2 = 5, तो x का मान क्या है?",
      en: "If x + 2 = 5, what is x?",
      optionsHi: ["1", "2", "3", "4"],
      optionsEn: ["1", "2", "3", "4"],
      answer: 2
    }
  ],
  science: [
    {
      hi: "पौधे अपना भोजन किस प्रक्रिया से बनाते हैं?",
      en: "By which process do plants make food?",
      optionsHi: ["श्वसन", "प्रकाश संश्लेषण", "पाचन", "उत्सर्जन"],
      optionsEn: ["Respiration", "Photosynthesis", "Digestion", "Excretion"],
      answer: 1
    },
    {
      hi: "पानी का रासायनिक सूत्र क्या है?",
      en: "What is the chemical formula of water?",
      optionsHi: ["CO2", "O2", "H2O", "NaCl"],
      optionsEn: ["CO2", "O2", "H2O", "NaCl"],
      answer: 2
    }
  ],
  sst: [
    {
      hi: "भारत की राजधानी क्या है?",
      en: "What is the capital of India?",
      optionsHi: ["पटना", "नई दिल्ली", "मुंबई", "कोलकाता"],
      optionsEn: ["Patna", "New Delhi", "Mumbai", "Kolkata"],
      answer: 1
    }
  ],
  hindi: [
    {
      hi: "'जल' का समानार्थी शब्द क्या है?",
      en: "What is a synonym of 'Jal' (water)?",
      optionsHi: ["आग", "पानी", "हवा", "धरती"],
      optionsEn: ["Fire", "Water", "Air", "Earth"],
      answer: 1
    }
  ],
  english: [
    {
      hi: "'Book' का हिंदी अर्थ क्या है?",
      en: "What is the Hindi meaning of 'Book'?",
      optionsHi: ["किताब", "कलम", "मेज", "कुर्सी"],
      optionsEn: ["Book", "Pen", "Table", "Chair"],
      answer: 0
    }
  ]
};

function setLanguage(lang) {
  language = lang;
  startQuiz();
}

function startQuiz() {
  clearInterval(timerInterval);
  current = 0;
  score = 0;
  timeLeft = 600;
  document.getElementById("result").classList.add("hidden");
  document.getElementById("question").classList.remove("hidden");
  document.getElementById("options").classList.remove("hidden");
  document.getElementById("nextBtn").classList.remove("hidden");
  showQuestion();
  updateTimer();
  timerInterval = setInterval(() => {
    timeLeft--;
    updateTimer();
    if (timeLeft <= 0) finishQuiz();
  }, 1000);
}

function showQuestion() {
  const subject = document.getElementById("subject").value;
  const list = questions[subject];
  const q = list[current];
  answered = false;

  document.getElementById("questionCount").textContent =
    (language === "hi" ? "प्रश्न " : "Question ") +
    (current + 1) + "/" + list.length;

  document.getElementById("question").textContent =
    language === "hi" ? q.hi : q.en;

  document.getElementById("options").innerHTML = "";
  const options = language === "hi" ? q.optionsHi : q.optionsEn;

  options.forEach((option, index) => {
    const btn = document.createElement("button");
    btn.className = "option";
    btn.textContent = option;
    btn.onclick = () => chooseAnswer(index, btn, q.answer);
    document.getElementById("options").appendChild(btn);
  });

  document.getElementById("progress").style.width =
    (current / list.length * 100) + "%";

  document.getElementById("nextBtn").textContent =
    language === "hi" ? "अगला प्रश्न" : "Next Question";
}

function chooseAnswer(index, button, answer) {
  if (answered) return;
  answered = true;

  const buttons = document.querySelectorAll(".option");
  buttons.forEach((btn, i) => {
    btn.disabled = true;
    if (i === answer) btn.classList.add("correct");
  });

  if (index === answer) {
    score++;
  } else {
    button.classList.add("wrong");
  }
}

function nextQuestion() {
  const subject = document.getElementById("subject").value;
  if (current < questions[subject].length - 1) {
    current++;
    showQuestion();
  } else {
    finishQuiz();
  }
}

function updateTimer() {
  const minutes = Math.floor(timeLeft / 60);
  const seconds = timeLeft % 60;
  document.getElementById("timer").textContent =
    (language === "hi" ? "समय: " : "Time: ") +
    minutes + ":" + String(seconds).padStart(2, "0");
}

function finishQuiz() {
  clearInterval(timerInterval);
  const subject = document.getElementById("subject").value;
  const total = questions[subject].length;

  document.getElementById("question").classList.add("hidden");
  document.getElementById("options").classList.add("hidden");
  document.getElementById("nextBtn").classList.add("hidden");
  document.getElementById("result").classList.remove("hidden");

  document.getElementById("score").textContent =
    (language === "hi" ? "आपका स्कोर: " : "Your score: ") +
    score + "/" + total;
}

startQuiz();
</script>
</body>
</html>
