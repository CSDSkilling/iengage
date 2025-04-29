---
layout: default
title:  "GitHub Actions"
category: "Comic"
sub-category: "Digital and App Innovation"
courses: [AZ-400, AZ-2008, AZ-2006, GH-200]
---


# GitHub Actions – Automation for the Win!

## Introduction
Welcome to the world of GitHub Actions – Automation for the Win! In this comic, we follow Alex, a curious student just beginning her coding journey. Frustrated by repetitive tasks like testing code manually, she turns to her tech-savvy friend Sam, who introduces her to the magic of GitHub Actions—a powerful tool built right into GitHub that can automate coding workflows.
Together, with the help of their floating AI assistant Botty, they explore the basics of automation: learning what workflows, jobs, steps, and actions are—and how all of these pieces work together to make a developer’s life easier. Set in a modern classroom and cozy coffee shop, this story makes it fun and easy to understand how GitHub Actions fits into real-world coding projects.

By the end of the comic, Alex has set up her first workflow—and is ready to automate like a pro!

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
         border-radius: 35px;
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
        <img id="carousel" class="carousel-image" src="./images/gh1.JPG" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

  <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: What does Azure Face Service do first when analyzing an image?</p>
                
                <label><input type="radio" name="question1" value="A">A) Identifies the emotion of the person </label><br>
                <label><input type="radio" name="question1" value="B">B) Matches the face to a database</label><br>
                <label><input type="radio" name="question1" value="C">C) Detects the face and provides its location</label><br>
                <label><input type="radio" name="question1" value="D"> D) Groups the face with others</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: What is the difference between ‘Verification’ and ‘Identification’ in Face Service?</p>
               <label><input type="radio" name="question2" value="A">A) Verification compares one face to many; Identification compares two faces</label><br>
                <label><input type="radio" name="question2" value="B">B) Verification compares two faces; Identification compares one face to many</label><br>
                <label><input type="radio" name="question2" value="C">C) Both are used only for emotion detection</label><br>
                <label><input type="radio" name="question2" value="D"> D) Verification uses live video; Identification uses photos</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: Which feature helps ensure the face in front of the camera is from a live person, not a spoof?</p>
               <label><input type="radio" name="question3" value="A">A) Emotion Detection</label><br>
                <label><input type="radio" name="question3" value="B">B) Find Similar</label><br>
                <label><input type="radio" name="question3" value="C">C) Liveness Detection</label><br>
                <label><input type="radio" name="question3" value="D"> D) Face Grouping</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: When would you use the 'Find Similar' feature?  </p>
               <label><input type="radio" name="question4" value="A">A) To analyze head pose</label><br>
                <label><input type="radio" name="question4" value="B">B) To match a face to lookalikes in a database</label><br>
                <label><input type="radio" name="question4" value="C">C) To detect sunglasses</label><br>
                <label><input type="radio" name="question4" value="D"> D) To verify biometric consent</label>
            </div>            
            <div class="knowledge-check-question">
                <p>Question 5: Which of the following is a requirement or rule when using Azure Face Service?</p>
               <label><input type="radio" name="question5" value="A">A) It can be used freely by U.S. police departments</label><br>
                <label><input type="radio" name="question5" value="B">B) You must follow Responsible AI guidelines and data protection laws like GDPR</label><br>
                <label><input type="radio" name="question5" value="C">C) You can store biometric data without consent</label><br>
                <label><input type="radio" name="question5" value="D"> D) The SDK only works with facial emotion recognition</label>
            </div>               
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
        const images = ["./images/gh1.JPG", "./images/gh2.JPG", "./images/gh3.JPG", "./images/gh4.JPG", "./images/gh5.JPG", "./images/gh6.JPG", "./images/gh7.JPG", "./images/gh8.JPG", "./images/gh9.JPG"];
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
                question1: 'C',
                question2: 'B',
                question3: 'C',
                question4: 'B',
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
