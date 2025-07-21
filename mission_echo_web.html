<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mission Echo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #0b0c10;
      color: #ffffff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }
    #game {
      display: none;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div id="login">
    <h2>Mission Echo – Belépés</h2>
    <input type="password" id="password" placeholder="Add meg a jelszót">
    <button onclick="checkPassword()">Belépés</button>
  </div>

  <div id="game">
    <h2>Mission Echo</h2>
    <p id="aiText"></p>
    <button onclick="startListening()">🎤 Válasz rögzítése</button>
    <p id="response"></p>
  </div>

  <script>
    const correctPassword = "mission2025";

    const missionSteps = [
      {
        prompt: "Ügynök, itt a központ. A Vízimolnár 10. előtt áll. Készen áll a küldetésre?",
        expected: ["igen", "kezdjük", "indulhatunk"],
        success: "Most induljon el a dombon túli kisbolthoz. Amint meglátja a bolt cégérét, álljon meg, jelentkezzen, és mondja a jelszót: foxtrottdeltacharlie.",
        fail: "Nem értettem. Készen áll a küldetésre?"
      },
      {
        prompt: "Mondja a jelszót, kérem.",
        expected: ["foxtrott"],
        success: "Kiváló. Most jöjjön a végső kérdés. A bolt feletti felirat utolsó betűje micsoda?",
        fail: "Ismételje meg a jelszót. Foxtrott."
      },
      {
        prompt: "A bolt felirata utolsó betűje?",
        expected: ["u"],
        success: "Küldetés teljesítve. Kiváló munka, ügynök.",
        fail: "Nézze meg újra alaposabban a feliratot!"
      }
    ];

    let currentStep = 0;

    function checkPassword() {
      const entered = document.getElementById('password').value;
      if (entered === correctPassword) {
        document.getElementById('login').style.display = 'none';
        document.getElementById('game').style.display = 'block';
        playStep();
      } else {
        alert("Hibás jelszó!");
      }
    }

    function speak(text) {
      const synth = window.speechSynthesis;
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = 'hu-HU';
      synth.speak(utterance);
      document.getElementById('aiText').innerText = text;
    }

    function playStep() {
      if (currentStep < missionSteps.length) {
        speak(missionSteps[currentStep].prompt);
      }
    }

    function startListening() {
      const recognition = new (window.SpeechRecognition || window.webkitSpeechRecognition)();
      recognition.lang = 'hu-HU';
      recognition.start();

      recognition.onresult = function(event) {
        const transcript = event.results[0][0].transcript.toLowerCase();
        document.getElementById('response').innerText = `Válasz: ${transcript}`;

        const step = missionSteps[currentStep];
        const matched = step.expected.length === 0 || step.expected.some(answer => transcript.includes(answer));

        if (matched) {
          speak(step.success);
          currentStep++;
          if (currentStep < missionSteps.length) {
            setTimeout(playStep, 3000);
          }
        } else {
          speak(step.fail);
        }
      }
    }
  </script>
</body>
</html>
