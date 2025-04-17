---
layout: default
title:  "Identity Protection - Risks"
category: "Comic"
sub-category: "Security, Compliance and Identity"
courses: [AZ-104, AZ-305, AZ-500]
---


# Enhancing Identity Protection in the Digital Age

## Introduction
In today's digital landscape, safeguarding user identities has become paramount. This comic illustrates a conversation between two individuals discussing the risks associated with user identity compromise and the advanced methods used to detect and mitigate these risks. The dialogue highlights the importance of understanding sign-in risks, detecting suspicious activities through machine learning, and employing robust identity protection measures.

<a href="./images/identityprot1.png">
  <img src="./images/identityprot1.png" alt="a boy and a girl sitting in a office space" class="img-fluid">
</a>
 

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .knowledge-check {
            margin-top: 50px;
        }
        .knowledge-check-question {
            margin-bottom: 20px;
        }
        .correct {
            color: green;
        }
        .incorrect {
            color: red;
        }
    </style>
</head>
<body>
  
  <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: You notice that your account has been flagged for user risk. What could be the reason?</p>
                
                <label><input type="radio" name="question1" value="A">A) You logged in from a new device.</label><br>
                <label><input type="radio" name="question1" value="B">B) Your credentials were found in a data breach.</label><br>
                <label><input type="radio" name="question1" value="C">C)  You accessed from an anonymous IP address.</label><br>
                <label><input type="radio" name="question1" value="D"> D) You used a weak password.</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: During a routine check, Entra ID flags a sign-in attempt as risky. What might be the cause?</p>
               <label><input type="radio" name="question2" value="A">A) The sign-in attempt came from an unfamiliar location.</label><br>
                <label><input type="radio" name="question2" value="B">B) The user changed their password recently.</label><br>
                <label><input type="radio" name="question2" value="C">C) The user logged in during regular business hours.</label><br>
                <label><input type="radio" name="question2" value="D"> D) The user accessed from a known device.</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: You receive a notification that your sign-in attempt was blocked due to high sign-in risk. What could be the reason?</p>
               <label><input type="radio" name="question3" value="A">A) You logged in from a new device.</label><br>
                <label><input type="radio" name="question3" value="B">B)  You accessed from an anonymous IP address.</label><br>
                <label><input type="radio" name="question3" value="C">C) Your credentials were found in a data breach.</label><br>
                <label><input type="radio" name="question3" value="D"> D) You used a weak password.</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: Entra ID detects suspicious activity on your account. What might be flagged as user risk?</p>
               <label><input type="radio" name="question4" value="A">A) Logging in from multiple locations in a short period.</label><br>
                <label><input type="radio" name="question4" value="B">B) Using a strong password.</label><br>
                <label><input type="radio" name="question4" value="C">C) Accessing from a known IP address.</label><br>
                <label><input type="radio" name="question4" value="D"> D) Logging in during regular business hours.</label>
            </div>            
            <div class="knowledge-check-question">
                <p>Question 5: You are informed that your account has been flagged for user risk due to compromised credentials. What should you do next?</p>
               <label><input type="radio" name="question5" value="A">A) Ignore the notification.</label><br>
                <label><input type="radio" name="question5" value="B">B) Change your password immediately.</label><br>
                <label><input type="radio" name="question5" value="C">C) Continue using the same credentials.</label><br>
                <label><input type="radio" name="question5" value="D"> D) Log in from a different device.</label>
            </div>               
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
      

            function checkAnswers() {
            const answers = {
                question1: 'B',
                question2: 'A',
                question3: 'B',
                question4: 'A',
                question5: 'B'
            
               
            };

            let score = 0;
            const form = document.getElementById('knowledgeCheckForm');
            const results = document.getElementById('results');
            results.innerHTML = '';

            for (const [question, correctAnswer] of Object.entries(answers)) {
                const selected = form.querySelector(`input[name="${question}"]:checked`);
                const questionElement = form.querySelector(`input[name="${question}"][value="${correctAnswer}"]`).parentElement;
                if (selected && selected.value === correctAnswer) {
                    score++;
                    questionElement.classList.add('correct');
                } else if (selected) {
                    selected.parentElement.classList.add('incorrect');
                    questionElement.classList.add('correct');
                } else {
                    questionElement.classList.add('correct');
                }
            }

  

            results.innerHTML = `You got ${score} out of ${Object.keys(answers).length} correct.`;
        }
    </script>
</body>
</html>
