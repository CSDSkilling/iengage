---
layout: default
title:  "Azure ML - Hyperparameter"
category: "Gamification123"
sub-category: "Data and AI"
courses: [AI-3016, AI-3018]
---
<div class="custom-container">
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
    <a href="./images/ai2.png">
        <img src="./images/ai2.png" alt="Alex is joined by a team of sidekicks" class="center-image">
    </a>
    <div class="card-container">
        <div class="card">
            <div class="card-front">Front 3</div>
            <div class="card-back">Back 3</div>
        </div>
        <div class="card">
            <div class="card-front">Front 4</div>
            <div class="card-back">Back 4</div>
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
    width: 150px;
    height: 200px;
    perspective: 1000px;
    margin-bottom: 20px;
    position: relative;
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
    transition: transform 0.6s;
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
    margin: 0 20px;
}
</style>
