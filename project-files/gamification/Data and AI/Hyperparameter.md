---
layout: default
title:  "Azure ML - Hyperparameter"
category: "Gamification123"
sub-category: "Data and AI"
courses: [AI-3016, AI-3018]
---
<div class="custom-container">
    <div class="card-container">
        <div class="card tall-card">
            <div class="card-front">
                represent the internal mechanisms of car, which are determined by the car's mechanical design
            </div>
        </div>
        <div class="card short-card" onclick="flipCard(this)">
            <div class="card-front clue-card">Clue</div>
            <div class="card-back">Back 2</div>
        </div>
    </div>
    <a href="./images/ai2.png">
        <img src="./images/ai2.png" alt="Alex is joined by a team of sidekicks" class="center-image">
    </a>
    <div class="card-container">
        <div class="card tall-card">
            <div class="card-front">
                represent the internal mechanisms of car, which are determined by the car's mechanical design
            </div>
        </div>
        <div class="card short-card" onclick="flipCard(this)">
            <div class="card-front clue-card">Clue</div>
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
    height: 150px; /* Increased by 50px */
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
}
</style>

<script>
function flipCard(card) {
    card.classList.toggle('flipped');
}
</script>
