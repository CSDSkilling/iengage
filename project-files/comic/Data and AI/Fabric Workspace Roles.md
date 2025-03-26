---
layout: default
title:  "Fabric Workspace Roles"
category: "Comic"
sub-category: "Data and AI"
courses: [DP-602,DP-603,DP-605]
---


# Exploring Microsoft Fabric Workspace Roles


## Introduction
Microsoft Fabric simplifies workspace management with four key roles Admin, Member, Contributor, and Viewer each defining a user’s level of access and responsibilities. While these roles ensure data governance and collaboration, understanding their real-world applications can be challenging.
In this conversation, Bob explores Microsoft Fabric roles but struggles to connect them with practical use cases. Juliet clarifies each role with relatable examples, helping Bob grasp how to assign roles effectively for a secure and well-structured workspace. This discussion serves as a practical guide to implementing role-based access control efficiently.

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
        <img id="carousel" class="carousel-image" src="./images/sunil-dialog.png" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

  <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: Bob is setting up a Microsoft Fabric workspace for his team. He needs full control over user permissions, workspace settings, and overall management.</p>
                
                <label><input type="radio" name="question1" value="A">A) Contributor</label><br>
                <label><input type="radio" name="question1" value="B">B) Member</label><br>
                <label><input type="radio" name="question1" value="C">C) Viewer</label><br>
                <label><input type="radio" name="question1" value="D"> D) Admin</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: Bob assigns a Contributor role to a business analyst. What is something the Contributor CANNOT do?</p>
                
                <label><input type="radio" name="question2" value="A">A) Edit and modify reports</label><br>
                <label><input type="radio" name="question2" value="B">B) Work with datasets and create dashboards</label><br>
                <label><input type="radio" name="question2" value="C">C) Share reports with others</label><br>
                <label><input type="radio" name="question2" value="D"> D) Build dataflows</label>
            </div>

            <div class="knowledge-check-question">
                 <p>Question 3: An executive in Juliet’s company needs access to reports and dashboards but does not need to modify or create content. Which role should they be assigned?</p>
                
                <label><input type="radio" name="question3" value="A">A) Admin</label><br>
                <label><input type="radio" name="question3" value="B">B) Member</label><br>
                <label><input type="radio" name="question3" value="C">C) Viewer</label><br>
                <label><input type="radio" name="question3" value="D"> D) Contributor</label>
            </div>

            <div class="knowledge-check-question">
                 <p>Question 4: Juliet is a senior data analyst in a company. She needs to create and modify reports, manage datasets, and share reports with others but does not need control over workspace settings.</p>
                
                <label><input type="radio" name="question4" value="A">A) Viewer</label><br>
                <label><input type="radio" name="question4" value="B">B) Contributor</label><br>
                <label><input type="radio" name="question4" value="C">C) Member</label><br>
                <label><input type="radio" name="question4" value="D"> D) Admin</label>
            </div>
                           
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
        const images = ["./images/sunil-dialog.png","./images/Slide1.PNG", "./images/Slide2.PNG", "./images/Slide3.PNG", "./images/Slide4.PNG", "./images/Slide5.PNG", "./images/Slide6.PNG", "./images/Slide7.PNG", "./images/Slide8.PNG", "./images/Slide9.PNG"];
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
               question3: 'C',
               question4: 'C'
                
               
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
