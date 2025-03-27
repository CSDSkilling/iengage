---
layout: default
title:  "GitHub Copilot Features"
category: "Gamification"
sub-category: "Digital and App Innovation"
courses: [AZ-2007]
---
# Improving Team Productivity with GitHub Copilot

## Introduction

A software development team at Contoso is working on a new project to develop a web application. The team is facing challenges with maintaining productivity due to the complexity of the codebase and the need for frequent code reviews and debugging. The team decides to leverage GitHub Copilot to enhance their workflow and improve efficiency.

<a href="./images/g1.jpeg">
  <img src="./images/g1.jpeg" alt="a group of developers in a office environment" class="img-fluid">
</a>

### Instructions for Flip Cards
Below are the questions. Each question is on one side of a flip card. Flip the card to see the answer. The answer can be **Copilot Chat** or  **Copilot Edit** or **Copilot Completion** or **Copilot Pull Request Summaries** or **Copilot Extensions**.


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <style>    
 
        .tile-container {
            display: flex;
            gap: 40px;
            margin-bottom: 20px;
            flex-wrap: wrap; /* Allow wrapping for better layout */
            justify-content: center; /* Center the tiles */
        }
        .tile {
            width: 300px;
            height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #e0f7fa, #80deea);
            
            color: black;
            border-radius: 40px;
            cursor: pointer;
            transition: transform 0.6s, background-color 0.3s;
            padding: 10px; /* Added padding */
            text-align: center; /* Center text */
            box-sizing: border-box; /* Include padding in size */
            position: relative;
            transform-style: preserve-3d;
            margin-bottom: 20px; /* Add margin for spacing */
        }
        .tile:hover {
            background: linear-gradient(135deg, #b2ebf2, #4dd0e1);
        }
        .tile .front, .tile .back {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 35px;
        }
        .tile .back {
            transform: rotateY(180deg);
            background: linear-gradient(135deg, #bbdefb, #64b5f6); 
              font-size: 24px;
        }
        .tile.flipped {
            transform: rotateY(180deg);
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="question"></div>
    <div class="tile-container">
        <div class="tile" onclick="checkAnswer(this, 'Copilot Chat')">
            <div class="front">A developer is stuck on implementing a complex algorithm and needs guidance on the best approach. Which GitHub Copilot feature should the developer use to get real-time assistance with coding questions?</div>
            <div class="back">Copilot Chat</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Copilot Edit')">
            <div class="front">The team has written a function to process user data but wants to optimize it for better performance. Which GitHub Copilot feature can suggest improvements and refinements to the existing code?</div>
            <div class="back">Copilot Edit</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Copilot Completion')">
            <div class="front">A developer is writing boilerplate code for a new class, including getter and setter methods. Which GitHub Copilot feature can automatically complete the repetitive code based on the context?</div>
            <div class="back">Copilot Completion</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Copilot Pull Request Summaries')">
            <div class="front">The team needs to generate a summary of changes made in a pull request to facilitate code review. Which GitHub Copilot feature can provide AI-generated summaries of pull request changes?</div>
            <div class="back">Copilot Pull Request Summaries</div>
        </div>      
        <div class="tile" onclick="checkAnswer(this, 'Copilot Extensions')">
            <div class="front"> A developer is integrating external tools into their workflow and wants to streamline the process within their IDE. Which GitHub Copilot feature allows integration of external tools into Copilot Chat?</div>
            <div class="back">Copilot Extensions</div>
        </div>      

    </div>

    <script>
        function checkAnswer(tile, answer) {
            if (tile.classList.contains('flipped')) {
                tile.classList.remove('flipped');
                setTimeout(() => {
                    tile.querySelector('.back').style.backgroundColor = '';
                    tile.querySelector('.back').textContent = '';
                }, 600); // Wait for the flip animation to complete
            } else {
                tile.querySelector('.back').style.backgroundColor = 'green';
                tile.querySelector('.back').textContent = answer;
                tile.classList.add('flipped');
            }
        }
    </script>
</body>
</html>
