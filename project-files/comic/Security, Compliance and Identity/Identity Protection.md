---
layout: default
title:  "Cosmos DB Read Consistency"
category: "Comic"
sub-category: "Data and AI"
courses: [AZ-204, AZ-305, DP-203]
---


# Cosmos DB Read Consistency

## Introduction
This image is a comic-style illustration depicting a business meeting where team members are discussing their next "Digital Transformation Plan." The conversation revolves around selecting an appropriate platform that can handle data cleaning, storage, and analysis. The team considers various options and ultimately decides on Microsoft Fabric as the solution that meets their needs.
<a href="./images/identityprot1.png">
  <img src="./images/identityprot1.png" alt="a boy and a girl sitting in a office space" class="img-fluid">
</a>
 

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Carousel</title>
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
                <p>Question 1: What consistency level was Alice initially using in her e-commerce application?</p>
                
                <label><input type="radio" name="question1" value="A">A) Strong Consistency</label><br>
                <label><input type="radio" name="question1" value="B">B) Bounded Staleness</label><br>
                <label><input type="radio" name="question1" value="C">C) Session Consistency</label><br>
                <label><input type="radio" name="question1" value="D"> D) Eventual Consistency</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: Which consistency level did Alice switch to in order to resolve the issue with shopping cart updates?</p>
               <label><input type="radio" name="question2" value="A">A) Strong Consistency</label><br>
                <label><input type="radio" name="question2" value="B">B) Bounded Staleness</label><br>
                <label><input type="radio" name="question2" value="C">C) Session Consistency</label><br>
                <label><input type="radio" name="question2" value="D"> D) Eventual Consistency</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: Which consistency level guarantees that reads always return the most recent write?</p>
               <label><input type="radio" name="question3" value="A">A) Strong Consistency</label><br>
                <label><input type="radio" name="question3" value="B">B) Bounded Staleness</label><br>
                <label><input type="radio" name="question3" value="C">C) Session Consistency</label><br>
                <label><input type="radio" name="question3" value="D"> D) Eventual Consistency</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: For a social media feed where posts are updated within a few minutes, which consistency level is ideal?</p>
               <label><input type="radio" name="question4" value="A">A) Strong Consistency</label><br>
                <label><input type="radio" name="question4" value="B">B) Bounded Staleness</label><br>
                <label><input type="radio" name="question4" value="C">C) Session Consistency</label><br>
                <label><input type="radio" name="question4" value="D"> D) Eventual Consistency</label>
            </div>            
            <div class="knowledge-check-question">
                <p>Question 5: Which consistency level ensures that reads never see out-of-order writes, maintaining the correct sequence of messages?</p>
               <label><input type="radio" name="question5" value="A">A) Strong Consistency</label><br>
                <label><input type="radio" name="question5" value="B">B) Bounded Staleness</label><br>
                <label><input type="radio" name="question5" value="C">C) Session Consistency</label><br>
                <label><input type="radio" name="question5" value="D"> D) Eventual Consistency</label>
            </div>               
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
        const images = ["./images/cd1.PNG", "./images/cd2.PNG", "./images/cd3.PNG", "./images/cd4.PNG", "./images/cd5.PNG", "./images/cd6.PNG", "./images/cd7.PNG"];
        let currentIndex = 0;

        function showImage(index) {
            const carousel = document.getElementById('carousel');
            carousel.src = images[index];
        }

        function nextImage() {
            currentIndex = (currentIndex + 1) % images.length;
            showImage(currentIndex);
        }

        function prevImage() {
            currentIndex = (currentIndex - 1 + images.length) % images.length;
            showImage(currentIndex);
        }

        function toggleEnlarge() {
            const carousel = document.getElementById('carousel');
            carousel.classList.toggle('enlarged');
        }

            function checkAnswers() {
            const answers = {
                question1: 'D',
                question2: 'C',
                question3: 'A',
                question4: 'B',
                question5: 'D'
            
               
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
