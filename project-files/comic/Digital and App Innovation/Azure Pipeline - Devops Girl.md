---
layout: default
title:  "Azure Devops Pipeline"
category: "Comic"
sub-category: "Digital and App Innovation"
courses: [AZ-400]
---


# DevOps Girl – Pipeline to the rescue!

## Introduction
In a near-futuristic world where software development powers everything from city infrastructure to education systems, stability and speed are essential—but chaos is never far behind. Deep in the digital realm, a dangerous force has awakened: the Glitch Beast. Born from corrupted code, broken builds, and unresolved errors, the Glitch Beast thrives in manual deployments, poor automation, and misconfigured pipelines. Every failed test and delayed release feeds its strength. Humanity’s ability to deploy code efficiently and securely is under siege.
But all is not lost.

From the heart of a high-tech training facility emerges a hero unlike any other: DevOps Girl. With an athletic build, a suit glowing with circuit patterns, and a utility belt stocked with debugging gadgets, she is more than just a coder—she is a symbol of clarity in the face of complexity. DevOps Girl has a gift: she can visualize and optimize CI/CD pipelines, debug code in midair, and summon test bots to battle errors at lightning speed. Her mission? To teach the world the power of Azure DevOps Pipelines and bring automation, precision, and peace to the tech world.

By her side is Leo, a bright and curious teen stepping into the world of software development. Eager to learn but easily overwhelmed, Leo represents every student starting their coding journey. With his trusty laptop plastered in stickers and his hoodie pulled tight, Leo brings a sense of humor and heart to the team. Under DevOps Girl’s guidance, he learns not just how to write code—but how to deliver it with confidence and control.
Together, they must face the Glitch Beast and all the confusion it brings. Through lessons in YAML syntax, pipeline stages, test automation, and production approvals, DevOps Girl shows Leo—and readers—how technology can be mastered, and how even the most intimidating systems can become tools of empowerment.
Welcome to DevOps Girl: Pipeline to the Rescue!
Where learning is heroic, automation is the weapon, and saving the day means shipping clean code.


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
        <img id="carousel" class="carousel-image" src="./images/ado1.JPG" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

  <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>Question 1: What is the main purpose of an Azure DevOps Pipeline?</p>
                
                <label><input type="radio" name="question1" value="A">A. To write frontend code </label><br>
                <label><input type="radio" name="question1" value="B">B. To automatically build, test, and deploy code</label><br>
                <label><input type="radio" name="question1" value="C">C. To manage cloud costs </label><br>
                <label><input type="radio" name="question1" value="D">D. To draw architecture diagrams</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: What file format is typically used to define an Azure Pipeline?</p>
               <label><input type="radio" name="question2" value="A">A. JSON</label><br>
                <label><input type="radio" name="question2" value="B">B. HTML </label><br>
                <label><input type="radio" name="question2" value="C">C. YAML </label><br>
                <label><input type="radio" name="question2" value="D">D. Markdown</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: Which section of a pipeline file defines the machine image used to run jobs?</p>
               <label><input type="radio" name="question3" value="A">A. trigger:</label><br>
                <label><input type="radio" name="question3" value="B">B. steps:  </label><br>
                <label><input type="radio" name="question3" value="C">C. pool: </label><br>
                <label><input type="radio" name="question3" value="D"> D. env:</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: What is the purpose of the script step in an Azure Pipeline?  </p>
               <label><input type="radio" name="question4" value="A">A. To create a database</label><br>
                <label><input type="radio" name="question4" value="B">B. To set user permissions</label><br>
                <label><input type="radio" name="question4" value="C">C. To run command-line instructions like install and test </label><br>
                <label><input type="radio" name="question4" value="D"> D. To define triggers</label>
            </div>            
            <div class="knowledge-check-question">
                <p>Question 5: How can you control when a deployment to production happens?</p>
               <label><input type="radio" name="question5" value="A">A. Add a delay timer </label><br>
                <label><input type="radio" name="question5" value="B">B. Use a manual approval step </label><br>
                <label><input type="radio" name="question5" value="C">C. Use a chatbot </label><br>
                <label><input type="radio" name="question5" value="D"> D. Add more npm install lines</label>
            </div>               
            <div class="knowledge-check-question">
                <p>Question 6: What does the trigger section in a YAML pipeline file do?</p>
               <label><input type="radio" name="question6" value="A">A. It lists environment variables </label><br>
                <label><input type="radio" name="question6" value="B">B. It chooses the operating system  </label><br>
                <label><input type="radio" name="question6" value="C">C. It defines when the pipeline should run  </label><br>
                <label><input type="radio" name="question6" value="D"> D. It sets up authentication</label>
            </div>               

            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    
  <script>
        const images = ["./images/ado1.JPG", "./images/ado2.JPG", "./images/ado3.JPG", "./images/ado4.JPG", "./images/ado5.JPG", "./images/ado6.JPG", "./images/ado7.JPG", "./images/ado8.JPG", "./images/ado9.JPG", "./images/ado10.JPG"];
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
                question2: 'C',
                question3: 'C',
                question4: 'C',
                question5: 'B',
                question6: 'C'
            
               
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
