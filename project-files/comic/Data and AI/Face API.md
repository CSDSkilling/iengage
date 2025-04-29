---
layout: default
title:  "Understanding Azure Face Service"
category: "Comic"
sub-category: "Data and AI"
courses: [AI-102]
---


# Understanding Azure Face Service

## Introduction
In a cutting-edge tech office buzzing with innovation, junior developer Jane begins her first week on the job, filled with excitement and curiosity. She's eager to learn the latest in AI and cloud technology, and today, she gets a one-on-one walkthrough with her mentor, Mario, a seasoned senior cloud architect. Their focus is Azure Face Service, a powerful tool that blends artificial intelligence with facial recognition. As they explore how it works, where it shines, and the responsibilities it demands, Jane begins to see how responsible AI can shape the future of digital identity and privacy. 

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
        <img id="carousel" class="carousel-image" src="./images/face1.JPG" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

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
        const images = ["./images/face1.JPG", "./images/face2.JPG", "./images/face3.JPG", "./images/face4.JPG", "./images/face5.JPG", "./images/face6.JPG", "./images/face7.JPG", "./images/face8.JPG"];
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
