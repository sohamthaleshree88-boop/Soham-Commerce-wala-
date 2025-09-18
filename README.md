# Soham-Commerce-wala-I can’t directly host the website for you, but ✅ I can give you a ready-made website file (index.html) with your chosen name “Soham Commerce Wala” as the title and branding.

Here’s the full code (you just need to upload it to GitHub Pages / Netlify):

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Soham Commerce Wala - Quiz Game</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(180deg, #eef2ff, #fefefe);
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }
    .container {
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 6px 20px rgba(0,0,0,0.1);
      max-width: 600px;
      width: 100%;
    }
    h1 {
      text-align: center;
      color: #2563eb;
    }
    .question {
      font-weight: bold;
      margin-bottom: 10px;
    }
    .options button {
      display: block;
      width: 100%;
      margin: 6px 0;
      padding: 10px;
      border-radius: 6px;
      border: 1px solid #ddd;
      background: #f9f9f9;
      cursor: pointer;
      font-size: 16px;
    }
    .options button:hover {
      background: #e0f2fe;
    }
    .options button.correct {
      background: #d1fae5;
      border-color: #16a34a;
    }
    .options button.wrong {
      background: #fee2e2;
      border-color: #dc2626;
    }
    #nextBtn {
      margin-top: 12px;
      padding: 10px 16px;
      border: none;
      background: #2563eb;
      color: white;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
    }
    #nextBtn:disabled {
      background: #93c5fd;
      cursor: not-allowed;
    }
    #result {
      text-align: center;
      font-size: 18px;
      margin-top: 20px;
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🎮 Soham Commerce Wala 🎮</h1>
    <div id="quiz">
      <div id="question" class="question"></div>
      <div id="options" class="options"></div>
      <button id="nextBtn" disabled>Next</button>
    </div>
    <div id="result"></div>
  </div>

  <script>
    const questions = [
      {
        question: "Debit the receiver, Credit the giver – is which accounting rule?",
        options: ["Personal Account", "Real Account", "Nominal Account"],
        answer: "Personal Account"
      },
      {
        question: "Which of these is a current asset?",
        options: ["Building", "Debtors", "Capital"],
        answer: "Debtors"
      },
      {
        question: "Who is known as the father of Economics?",
        options: ["Adam Smith", "Karl Marx", "Alfred Marshall"],
        answer: "Adam Smith"
      },
      {
        question: "Which tax is indirect?",
        options: ["Income Tax", "GST", "Property Tax"],
        answer: "GST"
      },
      {
        question: "The difference between total revenue and total cost is?",
        options: ["Profit", "Expense", "Liability"],
        answer: "Profit"
      }
    ];

    let current = 0;
    let score = 0;

    const questionEl = document.getElementById('question');
    const optionsEl = document.getElementById('options');
    const nextBtn = document.getElementById('nextBtn');
    const resultEl = document.getElementById('result');

    function showQuestion() {
      const q = questions[current];
      questionEl.textContent = `Q${current+1}. ${q.question}`;
      optionsEl.innerHTML = '';
      q.options.forEach(opt => {
        const btn = document.createElement('button');
        btn.textContent = opt;
        btn.onclick = () => selectAnswer(btn, q.answer);
        optionsEl.appendChild(btn);
      });
      nextBtn.disabled = true;
    }

    function selectAnswer(btn, correct) {
      const buttons = optionsEl.querySelectorAll('button');
      buttons.forEach(b => {
        b.disabled = true;
        if (b.textContent === correct) b.classList.add('correct');
      });
      if (btn.textContent !== correct) btn.classList.add('wrong');
      else score++;
      nextBtn.disabled = false;
    }

    nextBtn.onclick = () => {
      current++;
      if (current < questions.length) {
        showQuestion();
      } else {
        finishQuiz();
      }
    };

    function finishQuiz() {
      document.getElementById('quiz').style.display = 'none';
      resultEl.style.display = 'block';
      resultEl.innerHTML = `<p>Your Final Score: ${score}/${questions.length}</p>
        <p>${score === questions.length ? "🏆 Excellent! You are a Commerce Champion!" :
            score >= 3 ? "👏 Good Job! Keep practicing." :
            "📚 Need more practice. Don’t give up!"}</p>`;
    }

    showQuestion();
  </script>
</body>
</html>


---

✅ Next steps for you to make it live as a website with your name:

1. Copy the code above into a file called index.html.


2. Go to GitHub → create a free account.


3. Make a new repository called soham-commerce-wala.


4. Upload the index.html file.


5. In repo Settings → Pages → Enable GitHub Pages → choose main branch.


6. Your live link will be:
https://your-username.github.io/soham-commerce-wala/



👉 Do you want me to create the step-by-step GitHub upload tutorial with screenshots for you, so you can follow easily?

