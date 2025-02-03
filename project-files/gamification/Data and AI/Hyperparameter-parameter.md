---
layout: default
title:  "Hyperparameter vs parameter"
category: "Gamification123"
sub-category: "Data and AI"
courses: [DP-600]
---

# Differentiate Hyperparameter Vs Model Parameter in Azure Machine Learning


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image with Flippable Cards</title>
    <link rel="stylesheet" href="styles.css">
</head>

    <div class="container">
        <div class="card-container">
            <div class="card">
                <div class="card-front">Front 1</div>
                <div class="card-back">Back 1</div>
            </div>
            <div class="card">
                <div class="card-front">Front 2</div>
                <div class="card-back">Back 2</div>
            </div>
        </div>
        <img src="your-image.jpg" alt="Center Image" class="center-image">
        <div class="card-container">
            <div class="card">
                <div class="card-front">Front 3</div>
               Back 3</div>
            </div>
            <div class="card">
                <div class="card-front">Front 4</div>
                <div class="card-back">Back 4</div>
            </div>
        </div>
    </div>

.container {
    display: flex;
    align-items: center;
}

.card-container {
    display: flex;
    flex-direction: column;
    margin: 0 20px;
}

.card {
    width: 150px;
    height: 200px;
    perspective: 1000px;
    margin-bottom: 20px;
}

.card-front, .card-back {
    width: 100%;
    height: 100%;
    position: absolute;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    color: white;
    border-radius: 10px;
}

.card-front {
    background-color: #007bff;
}

.card-back {
    background-color: #28a745;
    transform: rotateY(180deg);
}

.card:hover .card-front {
    transform: rotateY(180deg);
}

.card:hover .card-back {
    transform: rotateY(360deg);
}

.center-image {
    width: 300px;
    height: auto;
}
</html>
