---
layout: default
title:  "Cosmos DB Read Consistency"
category: "Comic"
sub-category: "Modern Workplace"
courses: [AZ-204, AZ-305, DP-203]
---


# Cosmos DB Read Consistency

## Introduction
Olivia and Ethan, two IT professionals, discuss how to choose the right consistency levels when using Cosmos DB.
 

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
        <img id="carousel" class="carousel-image" src="./images/cd1.PNG" alt="Image Carousel" onclick="toggleEnlarge()">
        <button class="carousel-button" onclick="nextImage()">Next</button>
    </div>

</body>
</html>
