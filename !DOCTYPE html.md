<!DOCTYPE html>  
<html lang="es">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Online Grammar Quiz: Future Tenses</title>  
    <style>  
        :root {  
            --primary-color: #2b6cb0;  
            --primary-hover: #1e4e8c;  
            --bg-color: #f7fafc;  
            --card-bg: #ffffff;  
            --text-color: #2d3748;  
            --border-color: #e2e8f0;  
            --correct-color: #38a169;  
            --incorrect-color: #e53e3e;  
        }  
  
        body {  
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;  
            background-color: var(--bg-color);  
            color: var(--text-color);  
            line-height: 1.6;  
            margin: 0;  
            padding: 20px;  
        }  
  
        .quiz-container {  
            max-width: 800px;  
            margin: 0 auto;  
            background: var(--card-bg);  
            padding: 30px;  
            border-radius: 8px;  
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);  
        }  
  
        header {  
            text-align: center;  
            border-bottom: 2px solid var(--border-color);  
            padding-bottom: 20px;  
            margin-bottom: 30px;  
        }  
  
        h1 {  
            color: var(--primary-color);  
            margin: 0 0 10px 0;  
            font-size: 2rem;  
        }  
  
        .instructions {  
            background-color: #ebf8ff;  
            border-left: 4px solid var(--primary-color);  
            padding: 15px;  
            border-radius: 0 6px 6px 0;  
            margin-bottom: 30px;  
            font-size: 0.95rem;  
        }  
  
        .question-block {  
            margin-bottom: 25px;  
            padding: 20px;  
            border: 1px solid var(--border-color);  
            border-radius: 6px;  
            transition: all 0.2s ease;  
        }  
  
        .question-text {  
            font-weight: 600;  
            font-size: 1.1rem;  
            margin-bottom: 15px;  
        }  
  
        .options-container {  
            display: flex;  
            flex-direction: column;  
            gap: 10px;  
        }  
  
        .option-label {  
            display: flex;  
            align-items: center;  
            padding: 10px 15px;  
            border: 1px solid var(--border-color);  
            border-radius: 4px;  
            cursor: pointer;  
            transition: background-color 0.2s, border-color 0.2s;  
        }  
  
        .option-label:hover {  
            background-color: #f8fafc;  
            border-color: #cbd5e1;  
        }  
  
        .option-label input[type="radio"] {  
            margin-right: 12px;  
            width: 18px;  
            height: 18px;  
            accent-color: var(--primary-color);  
        }  
  
        /* Clases para la validación de respuestas */  
        .option-label.correct {  
            background-color: #c6f6d5 !important;  
            border-color: var(--correct-color) !important;  
            color: #22543d;  
            font-weight: bold;  
        }  
  
        .option-label.incorrect {  
            background-color: #fed7d7 !important;  
            border-color: var(--incorrect-color) !important;  
            color: #742a2a;  
        }  
  
        .btn-submit {  
            display: block;  
            width: 100%;  
            padding: 15px;  
            background-color: var(--primary-color);  
            color: white;  
            border: none;  
            border-radius: 6px;  
            font-size: 1.1rem;  
            font-weight: bold;  
            cursor: pointer;  
            transition: background-color 0.2s;  
            margin-top: 30px;  
        }  
  
        .btn-submit:hover {  
            background-color: var(--primary-hover);  
        }  
  
        #result-container {  
            margin-top: 30px;  
            padding: 20px;  
            border-radius: 6px;  
            text-align: center;  
            font-size: 1.3rem;  
            font-weight: bold;  
            display: none;  
        }  
  
        .result-success {  
            background-color: #c6f6d5;  
            color: #22543d;  
            border: 1px solid var(--correct-color);  
        }  
    </style>  
</head>  
<body>  
  
<div class="quiz-container">  
    <header>  
        <h1>English Grammar Quiz</h1>  
        <p style="color: #64748b; margin: 0;">Topic: Future Tenses (Will, Going to, Present Simple & Present Continuous)</p>  
    </header>  
  
    <div class="instructions">  
        <strong>Instructions:</strong> Read each sentence carefully and select the correct option to complete the blank space. Click "Submit Quiz" at the bottom when you are finished to see your score.  
    </div>  
  
    <form id="quizForm">  
        <!-- Question 1 -->  
        <div class="question-block" data-question="1">  
            <div class="question-text">1. My flight _____ at 10:00 a.m. tomorrow.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q1" value="a"> a) will leave</label>  
                <label class="option-label"><input type="radio" name="q1" value="b"> b) leaves</label>  
                <label class="option-label"><input type="radio" name="q1" value="c"> c) is leaving</label>  
                <label class="option-label"><input type="radio" name="q1" value="d"> d) going to leave</label>  
            </div>  
        </div>  
  
        <!-- Question 2 -->  
        <div class="question-block" data-question="2">  
            <div class="question-text">2. We _____ our cousins next weekend. The trip is already planned.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q2" value="a"> a) visit</label>  
                <label class="option-label"><input type="radio" name="q2" value="b"> b) will visit</label>  
                <label class="option-label"><input type="radio" name="q2" value="c"> c) are visiting</label>  
                <label class="option-label"><input type="radio" name="q2" value="d"> d) going to visit</label>  
            </div>  
        </div>  
  
        <!-- Question 3 -->  
        <div class="question-block" data-question="3">  
            <div class="question-text">3. Look at those black clouds! It _____ rain.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q3" value="a"> a) will</label>  
                <label class="option-label"><input type="radio" name="q3" value="b"> b) is going to</label>  
                <label class="option-label"><input type="radio" name="q3" value="c"> c) rains</label>  
                <label class="option-label"><input type="radio" name="q3" value="d"> d) raining</label>  
            </div>  
        </div>  
  
        <!-- Question 4 -->  
        <div class="question-block" data-question="4">  
            <div class="question-text">4. The concert _____ at 8:00 p.m.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q4" value="a"> a) starts</label>  
                <label class="option-label"><input type="radio" name="q4" value="b"> b) will start</label>  
                <label class="option-label"><input type="radio" name="q4" value="c"> c) is starting</label>  
                <label class="option-label"><input type="radio" name="q4" value="d"> d) start</label>  
            </div>  
        </div>  
  
        <!-- Question 5 -->  
        <div class="question-block" data-question="5">  
            <div class="question-text">5. “The phone is ringing!”<br>“Don’t worry, I _____ it.”</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q5" value="a"> a) answer</label>  
                <label class="option-label"><input type="radio" name="q5" value="b"> b) am answering</label>  
                <label class="option-label"><input type="radio" name="q5" value="c"> c) will answer</label>  
                <label class="option-label"><input type="radio" name="q5" value="d"> d) answered</label>  
            </div>  
        </div>  
  
        <!-- Question 6 -->  
        <div class="question-block" data-question="6">  
            <div class="question-text">6. She _____ the dentist on Monday.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q6" value="a"> a) sees</label>  
                <label class="option-label"><input type="radio" name="q6" value="b"> b) is seeing</label>  
                <label class="option-label"><input type="radio" name="q6" value="c"> c) will seeing</label>  
                <label class="option-label"><input type="radio" name="q6" value="d"> d) going see</label>  
            </div>  
        </div>  
  
        <!-- Question 7 -->  
        <div class="question-block" data-question="7">  
            <div class="question-text">7. I think our team _____ the game.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q7" value="a"> a) wins</label>  
                <label class="option-label"><input type="radio" name="q7" value="b"> b) is going to</label>  
                <label class="option-label"><input type="radio" name="q7" value="c"> c) will win</label>  
                <label class="option-label"><input type="radio" name="q7" value="d"> d) winning</label>  
            </div>  
        </div>  
  
        <!-- Question 8 -->  
        <div class="question-block" data-question="8">  
            <div class="question-text">8. Watch out! You _____ drop your phone.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q8" value="a"> a) will</label>  
                <label class="option-label"><input type="radio" name="q8" value="b"> b) are going to</label>  
                <label class="option-label"><input type="radio" name="q8" value="c"> c) drop</label>  
                <label class="option-label"><input type="radio" name="q8" value="d"> d) dropping</label>  
            </div>  
        </div>  
  
        <!-- Question 9 -->  
        <div class="question-block" data-question="9">  
            <div class="question-text">9. The bus _____ at 7:30 every morning.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q9" value="a"> a) leaves</label>  
                <label class="option-label"><input type="radio" name="q9" value="b"> b) is leaving</label>  
                <label class="option-label"><input type="radio" name="q9" value="c"> c) will leave</label>  
                <label class="option-label"><input type="radio" name="q9" value="d"> d) leaving</label>  
            </div>  
        </div>  
  
        <!-- Question 10 -->  
        <div class="question-block" data-question="10">  
            <div class="question-text">10. I _____ study harder this semester.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q10" value="a"> a) am going to</label>  
                <label class="option-label"><input type="radio" name="q10" value="b"> b) am studying</label>  
                <label class="option-label"><input type="radio" name="q10" value="c"> c) study</label>  
                <label class="option-label"><input type="radio" name="q10" value="d"> d) studies</label>  
            </div>  
        </div>  
  
        <!-- Question 11 -->  
        <div class="question-block" data-question="11">  
            <div class="question-text">11. “I can’t carry these books.”<br>“I _____ help you.”</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q11" value="a"> a) help</label>  
                <label class="option-label"><input type="radio" name="q11" value="b"> b) am helping</label>  
                <label class="option-label"><input type="radio" name="q11" value="c"> c) will help</label>  
                <label class="option-label"><input type="radio" name="q11" value="d"> d) helped</label>  
            </div>  
        </div>  
  
        <!-- Question 12 -->  
        <div class="question-block" data-question="12">  
            <div class="question-text">12. They _____ a party on Saturday night. Everything is ready.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q12" value="a"> a) have</label>  
                <label class="option-label"><input type="radio" name="q12" value="b"> b) are having</label>  
                <label class="option-label"><input type="radio" name="q12" value="c"> c) will have</label>  
                <label class="option-label"><input type="radio" name="q12" value="d"> d) having</label>  
            </div>  
        </div>  
  
        <!-- Question 13 -->  
        <div class="question-block" data-question="13">  
            <div class="question-text">13. The movie _____ at 6:45 p.m.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q13" value="a"> a) will start</label>  
                <label class="option-label"><input type="radio" name="q13" value="b"> b) starts</label>  
                <label class="option-label"><input type="radio" name="q13" value="c"> c) is starting</label>  
                <label class="option-label"><input type="radio" name="q13" value="d"> d) start</label>  
            </div>  
        </div>  
  
        <!-- Question 14 -->  
        <div class="question-block" data-question="14">  
            <div class="question-text">14. My sister _____ a new bicycle next month.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q14" value="a"> a) buys</label>  
                <label class="option-label"><input type="radio" name="q14" value="b"> b) is buying</label>  
                <label class="option-label"><input type="radio" name="q14" value="c"> c) is going to buy</label>  
                <label class="option-label"><input type="radio" name="q14" value="d"> d) bought</label>  
            </div>  
        </div>  
  
        <!-- Question 15 -->  
        <div class="question-block" data-question="15">  
            <div class="question-text">15. I promise I _____ tell anyone your secret.</div>  
            <div class="options-container">  
                <label class="option-label"><input type="radio" name="q15" value="a"> a) don’t tell</label>  
                <label class="option-label"><input type="radio" name="q15" value="b"> b) won’t</label>  
                <label class="option-label"><input type="radio" name="q15" value="c"> c) am not telling</label>  
                <label class="option-label"><input type="radio" name="q15" value="d"> d) not tell</label>  
            </div>  
        </div>  
  
        <button type="button" class="btn-submit" onclick="gradeQuiz()">Submit Quiz</button>  
    </form>  
  
    <div id="result-container" class="result-success"></div>  
</div>  
  
<script>  
    const correctAnswers = {  
        q1: 'b', q2: 'c', q3: 'b', q4: 'a', q5: 'c',  
        q6: 'b', q7: 'c', q8: 'b', q9: 'a', q10: 'a',  
        q11: 'c', q12: 'b', q13: 'b', q14: 'c', q15: 'b'  
    };  
  
    function gradeQuiz() {  
        let score = 0;  
        const totalQuestions = Object.keys(correctAnswers).length;  
        const form = document.getElementById('quizForm');  
  
        // Reiniciar estilos previos de validación  
        const allLabels = form.querySelectorAll('.option-label');  
        allLabels.forEach(label => {  
            label.classList.remove('correct', 'incorrect');  
        });  
  
        // Evaluar las respuestas de los estudiantes  
        for (let key in correctAnswers) {  
            const selectedOption = form.querySelector(`input[name="${key}"]:checked`);  
            const correctAnswerValue = correctAnswers[key];  
              
            // Buscar todas las opciones de la pregunta actual para aplicar los estilos visuales  
            const questionBlock = form.querySelector(`input[name="${key}"]`).closest('.question-block');  
            const options = questionBlock.querySelectorAll('.option-label');  
  
            options.forEach(label => {  
                const input = label.querySelector('input');  
                // Resaltar la respuesta correcta siempre en verde  
                if (input.value === correctAnswerValue) {  
                    label.classList.add('correct');  
                }  
                // Si el alumno seleccionó una opción incorrecta, resaltarla en rojo  
                if (selectedOption && selectedOption.value === input.value && selectedOption.value !== correctAnswerValue) {  
                    label.classList.add('incorrect');  
                }  
            });  
  
            if (selectedOption && selectedOption.value === correctAnswerValue) {  
                score++;  
            }  
        }  
  
        // Mostrar cuadro de resultados  
        const resultContainer = document.getElementById('result-container');  
        resultContainer.innerHTML = `Your Score: ${score} / ${totalQuestions} (${Math.round((score/totalQuestions)*100)}%)`;  
        resultContainer.style.display = 'block';  
          
        // Hacer scroll automático hacia los resultados  
        resultContainer.scrollIntoView({ behavior: 'smooth' });  
    }  
</script>  
  
</body>  
</html>  
