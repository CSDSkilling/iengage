---
layout: default
title:  "Azure Policy and RBAC"
category: "Comic123"
sub-category: "Security, Compliance and Identity"
courses: [AZ-104, AZ-305, AZ-500]
---


# Overcoming Access Control Challenges with Azure Policy and RBAC

## Introduction
In this dialog, a man and a lady discuss a real-time challenge they faced with unauthorized access to project files. They explore how implementing Azure Policy and Role-Based Access Control (RBAC) helped them resolve the issue effectively, ensuring better security and access management within their organization. 

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
        <img id="carousel" class="carousel-image" src="./images/rp0.png" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

 <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: How can Azure RBAC help in managing access to sensitive project files?</p>
                
                <label><input type="radio" name="question1" value="A">A) By allowing unrestricted access to all users</label><br>
                <label><input type="radio" name="question1" value="B">B) By assigning permissions based on user roles</label><br>
                <label><input type="radio" name="question1" value="C">C) By encrypting all project files</label><br>
                <label><input type="radio" name="question1" value="D"> D)By deleting sensitive files after use</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: What is a key component of Azure's data protection policy that supports RBAC implementation?</p>
               <label><input type="radio" name="question2" value="A">A) Unlimited access for all employees</label><br>
                <label><input type="radio" name="question2" value="B">B) Role-based access control guidelines</label><br>
                <label><input type="radio" name="question2" value="C">C) Regular deletion of old files</label><br>
                <label><input type="radio" name="question2" value="D"> D) Public sharing of sensitive information</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: How can Azure Policy help enforce compliance across different Azure resources?</p>
               <label><input type="radio" name="question3" value="A">A) By allowing unrestricted access to all resources</label><br>
                <label><input type="radio" name="question3" value="B">B) By defining and enforcing rules on resource configurations</label><br>
                <label><input type="radio" name="question3" value="C">C) By encrypting all data automatically</label><br>
                <label><input type="radio" name="question3" value="D"> D) By deleting non-compliant resources</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: What is the role of Azure Policy in managing resource locks and preventing accidental changes?</p>
               <label><input type="radio" name="question4" value="A">A) Azure Policy automatically deletes resources after a certain period</label><br>
                <label><input type="radio" name="question4" value="B">B) Azure Policy can enforce resource locks to prevent accidental deletion or modification</label><br>
                <label><input type="radio" name="question4" value="C">C) Azure Policy allows unrestricted changes to all resources</label><br>
                <label><input type="radio" name="question4" value="D"> D) Azure Policy encrypts all resource data</label>
            </div>            
           
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>


    
  <script>
        const images = ["./images/rp0.png", "./images/rp1.PNG", "./images/rp2.PNG", "./images/rp3.PNG", "./images/rp4.PNG"];
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
                question2: 'B',
                question3: 'B',
                question4: 'B'            
               
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
