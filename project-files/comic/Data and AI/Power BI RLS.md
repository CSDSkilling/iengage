---
layout: default
title:  "Power BI - RLS"
category: "Comic"
sub-category: "Data and AI"
courses: [PL-300, DP-605]
---


# Exploring Power BI Row-Level security


## Introduction
Controlling data access is crucial in any organization, and Row-Level Security (RLS) in Microsoft Fabric helps restrict data visibility based on user roles or attributes. However, understanding when to use Static vs. Dynamic RLS can be challenging. In this conversation, Amit is exploring RLS and seeks guidance from Sara on how to implement it in real-world scenarios. Sara explains how Static RLS works well for predefined access rules, while Dynamic RLS offers a scalable approach by filtering data dynamically based on user attributes. Through practical examples, Amit gains clarity on choosing the right approach for his project, ensuring secure and efficient data access.


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
        <img id="carousel" class="carousel-image" src="./images/pbrole1.png" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

  <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: A multinational company has a Sales dataset containing sales records for different countries. The company wants each country’s manager to see only their own country’s data. The security roles will not change frequently. Which RLS approach is the best fit?</p>
                
                <label><input type="radio" name="question1" value="A">A) No RLS is needed since all managers can see all data</label><br>
                <label><input type="radio" name="question1" value="B">B) Static RLS, as each manager’s access is predefined and does not change dynamically</label><br>
                <label><input type="radio" name="question1" value="C">C) Dynamic RLS, as access should be determined based on user attributes at login</label><br>
                <label><input type="radio" name="question1" value="D"> D) Assign separate datasets for each country instead of using RLS</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: A company has a Customer Support dashboard where support agents should only see tickets assigned to them. The dataset contains a User Table that maps agents to their respective tickets using their email ID. Which implementation method should be used?</p>
                
                <label><input type="radio" name="question2" value="A">A) Apply a filter where support_agent = ‘John Doe’ for each user</label><br>
                <label><input type="radio" name="question2" value="B">B) Use a User Table and filter data dynamically based on the logged-in user’s email</label><br>
                <label><input type="radio" name="question2" value="C">C) Create a separate dashboard for each agent</label><br>
                <label><input type="radio" name="question2" value="D"> D) Assign each agent an admin role so they can filter their own data manually</label>
            </div>

          
                           
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
        const images = ["./images/pbrole1.png","./images/pbrole2.PNG", "./images/pbrole3.PNG", "./images/pbrole4.PNG", "./images/pbrole4.PNG", "./images/pbrole6.PNG", "./images/pbrole7.PNG", "./images/pbrole8.PNG"];
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
