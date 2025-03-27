---
layout: default
title:  "Types of Copilot"
category: "Gamification"
sub-category: "Modern Workspace"
courses: [MS-4005, MS-4002]
---
# A meeting room at a tech company.

## Introduction

Alex, a consultant is discussing with Debra, business decision-maker, on potential adoption of Copilot solutions.

### Instructions for Flip Cards
Below are the questions. Each question is on one side of a flip card. Flip the card to see the answer. The answer can be **Microsoft Copilot** or **Microsoft 365 Copilot** or **Microsoft Security Copilot** or **GitHub Copilot**.


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
            height: 200px;
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
        <div class="tile" onclick="checkAnswer(this, 'Microsoft Copilot')">
            <div class="front">Used for personal tasks, Free consumer version, Uses information from the internet</div>
            <div class="back">Microsoft Copilot</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Microsoft 365 Copilot')">
            <div class="front">Used for work tasks, Licensed by your work organization, Get in-app experiences in your Microsoft 365 apps, like Teams, Word, Excel, PowerPoint, and Outlook, Can access user-accessible work data (via Microsoft Graph) to generate Grounded response</div>
            <div class="back">Microsoft 365 Copilot</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Microsoft Security Copilot')">
            <div class="front">Used by security professionals for incident investigation, threat hunting, intelligence gathering, posture management.
Licensed by your work organization,
Can access work data that the security professional's Microsoft Entra account has access to.
Integrates with other services, like Microsoft Defender XDR, Microsoft Purview, Microsoft Intune, Microsoft Entra, and some non-Microsoft services</div>
            <div class="back">Microsoft Security Copilot</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'GitHub Copilot')">
            <div class="front">Used by developers as AI coding assistant for writing code,
Licensed by your work organization,
Developers can Get code suggestions as they type and Ask for help when writing your code</div>
            <div class="back">GitHub Copilot</div>
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
