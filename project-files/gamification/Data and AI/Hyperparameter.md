---
layout: default
title:  "Azure ML - Hyperparameter"
category: "Gamification123"
sub-category: "Data and AI"
courses: [AI-3016, AI-3018]
---
# Perform hyperparameter tuning with Azure Machine Learning

## Introduction

#### Parameter
* Parameters are values within a machine learning model that are determined from the training data. They are internal configuration variables that can be estimated from the data.<br>
#### Hyperparameter
* Hyperparameters are values you set to influence the training process of a machine learning model. They are not derived from the training data but are used to configure how the model is trained to improve its accuracy.


## How to play
What is a hyperparameter vs model parameter?
Imagine your machine learning model is like a car. We can compare different parts of the car to hyperparameters and parameters in a machine learning model.



<div class="custom-container">
    <div class="card-container">
        <div class="card tall-card">
            <div class="card-front">
                Represent the internal mechanisms of car, which are determined by the car's mechanical design. Example: engine, gears, tires
            </div>
        </div>
        <div class="card short-card" onclick="flipCard(this)">
            <div class="card-front clue-card"><i>Clue</i></div>
            <div class="card-back">Parameter</div>
        </div>
    </div>
    <a href="./images/car1.png">
        <img src="./images/car1.png" alt="picture of a car" class="center-image">
    </a>
    <div class="card-container">
        <div class="card tall-card">
            <div class="card-front">
                Represent external settings, which you adjust according to a personal preference or a specific journey. Example: angle of your steering wheel,  the position of your seat
            </div>
        </div>
        <div class="card short-card" onclick="flipCard(this)">
            <div class="card-front clue-card"><i>Clue</i></div>
            <div class="card-back">Hyperparameter</div>
        </div>
    </div>
</div>

<style>
.custom-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px; /* Adjust as needed to fit your layout */
}

.card-container {
    display: flex;
    flex-direction: column;
    margin: 0 20px;
}

.card {
    width: 250px;
    perspective: 1000px;
    margin-bottom: 20px;
    position: relative;
    cursor: pointer;
}

.tall-card {
    height: 300px; /* Increased by 100px */
}

.short-card {
    height: 50px; /* Increased by 50px */
}

.card-front, .card-back {
    width: 100%;
    height: 100%;
    position: absolute;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 16px;
    color: white;
    border-radius: 10px;
    transition: transform 0.6s;
    padding: 10px;
    box-sizing: border-box;
    text-align: center;
}

.card-front {
    background-color: #007bff;
}

.card-back {
    background-color: #28a745;
    transform: rotateY(180deg);
}

.card.flipped .card-front {
    transform: rotateY(180deg);
}

.card.flipped .card-back {
    transform: rotateY(360deg);
}

.center-image {
    width: 500px;
    height: auto;
    margin: 0 20px;
}

.clue-card {
    background-color: #ffcc00; /* Dark yellow */
    color: black; /* Text color for better contrast */
    height: auto;
}
</style>

<script>
function flipCard(card) {
    card.classList.toggle('flipped');
}
</script>
