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
**Section 1:** <br>
What is a hyperparameter vs model parameter?

Imagine your machine learning model is like a car. We can compare different parts of the car to hyperparameters and parameters in a machine learning model.


<div class="custom-container">
    <a href="./images/car1.png">
        <img src="./images/car1.png" alt="picture of a car" class="center-image">
    </a>
    <div class="cards-row">
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
        <div class="card-container">
            <div class="card tall-card">
                <div class="card-front">
                    Represent external settings, which you adjust according to a personal preference or a specific journey. Example: angle of your steering wheel, the position of your seat
                </div>
            </div>
            <div class="card short-card" onclick="flipCard(this)">
                <div class="card-front clue-card"><i>Clue</i></div>
                <div class="card-back">Hyperparameter</div>
            </div>
        </div>
    </div>
</div>

<div class="content-section">
    <h2>Configure a sampling method for hyperparameter tuning in Azure Machine Learning</h2>
    <p>Azure Machine Learning supports various sampling methods for hyperparameter optimization. The specific values used in hyperparameter tuning depend on the type of sampling method:</p>
    <ul>
        <li><strong>Grid Sampling</strong> tries every possible combination of values in the search space.</li>
        <li><strong>Random Sampling</strong> randomly selects a value for hyperparameter from the search space.</li>
    </ul>
</div>

<div class="custom-container">
    <a href="./images/car2.png">
        <img src="./images/car2.png" alt="picture of a car" class="center-image">
    </a>
    <div class="cards-row">
        <div class="card-container">
            <div class="card tall-card">
                <div class="card-front">
                  This is like checking how the car drives when you change the seat position, mirror angles, and steering wheel height in every possible way. In ML, this method tries every possible combination of hyperparameters in the search space to find what works best.
                </div>
            </div>
            <div class="card short-card" onclick="flipCard(this)">
                <div class="card-front clue-card"><i>Clue</i></div>
                <div class="card-back">Grid Sampling </div>
            </div>
        </div>
        <div class="card-container">
            <div class="card tall-card">
                <div class="card-front">
                  Instead of changing everything step by step, this is like randomly tweaking things in car (e.g., adjusting the air conditioning, the radio volume, etc). It’s quicker and can sometimes give you a surprisingly good setting without having to try everything.

                </div>
            </div>
            <div class="card short-card" onclick="flipCard(this)">
                <div class="card-front clue-card"><i>Clue</i></div>
                <div class="card-back">Random Sampling </div>
            </div>
        </div>
    </div>
</div>


<div class="content-section">
    <h2>Work with environments in Azure Machine Learning</h2>
    <p>In Azure Machine Learning, environments encapsulate the environment where your machine learning task happens, specifying software packages, environment variables, and settings around your training and scoring scripts. An Azure Machine Learning environment includes the dependencies (like software runtime and libraries) needed to run your training and scoring script on your compute resource.

There are two types of environments:
</p>
    <ul>
        <li><strong>Curated environment:</strong> are available to you in Azure Machine Learning by default. Curated Environment are predefined environments containing popular ML frameworks and tools.</li>
        <li><strong>Custom environment: </strong> You can create and manage your own custom environments. This allows you to define consistent, reusable runtime contexts for your experiments.</li>
    </ul>
</div>

<div class="custom-container">
    <a href="./images/car2.png">
        <img src="./images/cookie1.png" alt="picture of a car" class="center-image">
    </a>
    <div class="cards-row">
        <div class="card-container">
            <div class="card tall-card">
                <div class="card-front">
           Looking to use store-bought cookie dough (Environment) & reuse the cookie dough for the cookie (Machine Learning experiment) you are making?It's provided by Azure ML and is available in your workspace.These precreated environments allow for faster deployment time. 

                </div>
            </div>
            <div class="card short-card" onclick="flipCard(this)">
                <div class="card-front clue-card"><i>Clue</i></div>
                <div class="card-back">Curated Environment </div>
            </div>
        </div>
        <div class="card-container">
            <div class="card tall-card">
                <div class="card-front">
               Do you want to make new cookie dough (Environment) for each cookie (Machine Learning experiment) you are making? You're responsible for setting up your ___ and installing every package that your training script needs on the compute target. 


                </div>
            </div>
            <div class="card short-card" onclick="flipCard(this)">
                <div class="card-front clue-card"><i>Clue</i></div>
                <div class="card-back">Custom Environment  </div>
            </div>
        </div>
    </div>
</div>

<style>
.custom-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px; /* Adjust as needed to fit your layout */
}

.cards-row {
    display: flex;
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
    margin: 20px; /* Adjust margin to ensure spacing */
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
