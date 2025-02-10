---
layout: default
title:  "AI Search Index in Action"
category: "Comic"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3016]
---

# Understanding Azure AI Search Index: Structure, Size, and Optimization

## Introduction
In this scenario, team members in a conference room are discussing the intricacies of Azure AI Search Index. They delve into how the search index functions, its physical structure, and the factors influencing its size. The conversation highlights the internal management of the index by Microsoft, the importance of schema definition, and the role of field attributes and suggesters in optimizing search performance. This dialogue aims to provide a comprehensive understanding of how to effectively utilize Azure AI Search Index for efficient and secure data retrieval.

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
        <img id="carousel" class="carousel-image" src="./images/ai1.png" alt="Image Carousel" onclick="toggleEnlarge()">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

    <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>1. What is the primary purpose of separating the search index from the primary data stores in Azure AI Search?</p>
                <label><input type="radio" name="question1" value="A"> A) To reduce storage costs</label><br>
                <label><input type="radio" name="question1" value="B"> B) To ensure faster response times and better performance</label><br>
                <label><input type="radio" name="question1" value="C"> C) To simplify data management</label><br>
                <label><input type="radio" name="question1" value="D"> D) To enhance data security</label>
            </div>
            <div class="knowledge-check-question">
                <p>2. Which of the following scenarios enable the Azure AI Search service to connect to the source data for indexing?</p>
                <label><input type="radio" name="question2" value="A"> A) Full text search</label><br>
                <label><input type="radio" name="question2" value="B"> B) Indexer-driven indexing</label><br>
                <label><input type="radio" name="question2" value="C"> C) Vector search</label><br>
                <label><input type="radio" name="question2" value="D"> D) Hybrid search</label>
            </div>
            <div class="knowledge-check-question">
                <p>3. What factors determine the size of an Azure AI Search index?</p>
                <label><input type="radio" name="question3" value="A"> A) The number of users accessing the index</label><br>
                <label><input type="radio" name="question3" value="B"> B) The quantity and composition of documents, attributes on individual fields, and index configuration</label><br>
                <label><input type="radio" name="question3" value="C"> C) The frequency of data updates</label><br>
                <label><input type="radio" name="question3" value="D"> D) The type of data storage used</label>
            </div>
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    <script>
        const images = ["./images/ai1.png", "./images/ai2.png", "./images/ai3.png"];
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
                question3: 'B'
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
