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
                <p>Question 1: What is the main purpose of GitHub Actions?</p>
                
                <label><input type="radio" name="question1" value="A">A) To write code automatically  </label><br>
                <label><input type="radio" name="question1" value="B">B) To automate workflows such as testing, building, or deploying code</label><br>
                <label><input type="radio" name="question1" value="C">C) To store files on GitHub  </label><br>
                <label><input type="radio" name="question1" value="D"> D) To design user interfaces</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 2: Where are GitHub workflow files typically stored?</p>
               <label><input type="radio" name="question2" value="A">A) In the root of the repository  </label><br>
                <label><input type="radio" name="question2" value="B">B) In a folder named `src/workflows` </label><br>
                <label><input type="radio" name="question2" value="C">C) In the `.github/workflows/` directory  </label><br>
                <label><input type="radio" name="question2" value="D"> D) In a folder called `automation/`</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 3: What file format is used to define workflows in GitHub Actions?</p>
               <label><input type="radio" name="question3" value="A">A) `.html`  </label><br>
                <label><input type="radio" name="question3" value="B">B) `.exe`  </label><br>
                <label><input type="radio" name="question3" value="C">C) `.yml` or `.yaml`  </label><br>
                <label><input type="radio" name="question3" value="D"> D) `.json`</label>
            </div>
            <div class="knowledge-check-question">
                <p>Question 4: What are the main building blocks of a GitHub Actions workflow?  </p>
               <label><input type="radio" name="question4" value="A">A) Pages, Repos, Commits </label><br>
                <label><input type="radio" name="question4" value="B">B) Scripts, Branches, Merges  </label><br>
                <label><input type="radio" name="question4" value="C">C) Workflows, Jobs, Steps, Actions  </label><br>
                <label><input type="radio" name="question4" value="D"> D) Tokens, Secrets, Forks</label>
            </div>            
            <div class="knowledge-check-question">
                <p>Question 5: What happens when you push new code to a GitHub repository with an active workflow?</p>
               <label><input type="radio" name="question5" value="A">A) The repository is deleted  </label><br>
                <label><input type="radio" name="question5" value="B">B) A new branch is created  </label><br>
                <label><input type="radio" name="question5" value="C">C) The defined workflow is triggered automatically  </label><br>
                <label><input type="radio" name="question5" value="D"> D) Nothing happens until you manually start it</label>
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
                question5: 'C'
            
               
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
