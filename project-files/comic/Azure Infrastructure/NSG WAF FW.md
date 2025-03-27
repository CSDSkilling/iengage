---
layout: default
title:  "Network Security Options"
category: "Comic"
sub-category: "Azure Infrastructure"
courses: [AZ-104, AZ-700, AZ-305, AZ-500]
---


# Understanding Azure Network Security Options: NSGs, Azure Firewall, and WAF"

## Introduction
In this dialogue, Bob and Sally discuss transitioning from on-premises infrastructure to Azure and the need to find a suitable network security alternative. Bob mentions their current use of a Cisco firewall and seeks to understand the differences between Azure's Network Security Groups (NSGs), Azure Firewall, and Web Application Firewall (WAF). Sally explains each service's purpose and use cases:

**NSGs**: Filter network traffic within an Azure Virtual Network, controlling traffic at the network level.<br>
**Azure** Firewall: A managed, cloud-based service providing advanced threat protection and centralized security policy management.<br>
**WAF**: Protects web applications from common threats and vulnerabilities, typically used with Azure Application Gateway or Azure Front Door.<br>

Sally emphasizes the importance of using these services to ensure security and compliance in their Azure environment. Bob appreciates the clarification and thanks Sally for the detailed explanation. 

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
        <img id="carousel" class="carousel-image" src="./images/Slide1.PNG" alt="Image Carousel" onclick="toggleEnlarge()" class="img-fluid">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

  

    
  <script>
        const images = ["./images/Slide1.PNG", "./images/Slide2.PNG", "./images/Slide3.PNG", "./images/Slide4.PNG", "./images/Slide5.PNG", "./images/Slide6.PNG", "./images/Slide7.PNG", "./images/Slide8.PNG"];
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
