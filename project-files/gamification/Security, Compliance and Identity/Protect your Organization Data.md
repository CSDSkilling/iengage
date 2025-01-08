---
layout: default
title:  "Protect your Organization Data"
category: "Gamification"
sub-category: "Security, Compliance and Identity"
courses: [SC-400, SC-5003]
---
# Protect your Organization Data

## Introduction

You are the Information Security specialist of DataGuardians Inc., an organization that handles lots of sensitive data like PII and financial data. All these data belongs to your customers and partners. You are designated to design data security solutions using Microsoft Purview, that will help DataGuardians Inc. to discover, classify and protect sensitive information.

### Instructions for Flip Cards
Below are the questions. Each question is on one side of a flip card. Flip the card to see the answer. The answer can be Sensitive Information Types (SIT) or Sensitivity Labels or Retention Labels or Data Loss Prevention (DLP).


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
        <div class="tile" onclick="checkAnswer(this, 'Sensitive Information Types (SIT)')">
            <div class="front">What pattern-based classifiers can you use to detect and classify sensitive information such as social security numbers, credit card numbers, and bank account numbers?</div>
            <div class="back">Sensitive Information Types (SIT)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Sensitivity Labels')">
            <div class="front">Which labels can help your organization to classify and protect sensitive information by labelling documents and emails to ensure that only authorized users can access or modify them?</div>
            <div class="back">Sensitivity Labels</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Retention Labels')">
            <div class="front">Which labels can help your organization to manage the lifecycle of data by specifying how long content should be kept and what actions should be taken at the end of the retention period?</div>
            <div class="back">Retention Labels</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Data Loss Prevention (DLP)')">
            <div class="front">When your organization needs to detect and prevent the unintentional sharing of sensitive information, which set of capabilities in Microsoft Purview will you use?</div>
            <div class="back">Data Loss Prevention (DLP)</div>
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
