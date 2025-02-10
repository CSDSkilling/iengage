---
layout: default
title:  "Copilot User Enablement"
category: "Comic"
sub-category: "Modern Workplace"
courses: [MS-4007, MS-4014]
---


# Copilot User Enablement Framework

## Introduction
Olivia and Ethan, two IT professionals, discuss how to successfully adopt Microsoft 365 Copilot in their organization. Olivia takes the lead in explaining the framework, while Ethan asks questions and provides insights.
 

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Carousel</title>
    <style>
        .carousel-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 50px;
        }
        .carousel-image {
            width: 800px;
            max-height: 700px;
            transition: transform 0.3s ease;
            cursor: pointer;
        }
        .carousel-image.enlarged {
            transform: scale(1.5);
        }
        .carousel-button {
            padding: 10px 20px;
            margin: 0 10px;
            cursor: pointer;
        }
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
    <div class="carousel-container">
        <button class="carousel-button" onclick="prevImage()">Previous</button>
        <img id="carousel" class="carousel-image" src="./images/Slide1.PNG" alt="Image Carousel" onclick="toggleEnlarge()">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

    <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: Setting the Stage</p>
                <p>What is the key approach to successfully adopting Microsoft 365 Copilot?</p>
                <label><input type="radio" name="question1" value="A">A) Deploy the tool as quickly as possible</label><br>
                <label><input type="radio" name="question1" value="B">B) Use the People First strategy</label><br>
                <label><input type="radio" name="question1" value="C">C) Focus only on technical readiness</label><br>
                <label><input type="radio" name="question1" value="D"> D) Rely on employees to figure it out themselves</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: Adoption Phase</p>
                <p>What is the primary goal of the Adoption phase?</p>
                <label><input type="radio" name="question2" value="A">A) Getting as many employees as possible to use Copilot</label><br>
                <label><input type="radio" name="question2" value="B"> B) Making AI a natural part of users' daily workflows</label><br>
                <label><input type="radio" name="question2" value="C">C) Replacing employees with AI</label><br>
                <label><input type="radio" name="question2" value="D">D) Using AI only for leadership teams</label>
            </div>
     
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    <script>
        const images = ["./images/Slide1.PNG", "./images/Slide2.PNG", "./images/Slide3.PNG", "./images/Slide4.PNG", "./images/Slide5.PNG", "./images/Slide6.PNG"];
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
                question1: 'B',
                question2: 'B'
               
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
