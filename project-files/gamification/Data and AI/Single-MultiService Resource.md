---
layout: default
title:  "Single Service Vs Multi-Service Resource"
category: "Gamification"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3003, AI-3004]
---
# Smart City Initiative - Single Service Vs Multi-Service Account

## Introduction

City of Innovaville is launching a Smart City Initiative to improve urban living through technology. The city plans to use Azure AI services to enhance various aspects of city management, including traffic monitoring, public safety, and environmental monitoring.

#### Single Service Example: Traffic Monitoring
For traffic monitoring, Innovaville decides to use Azure Computer Vision to analyze live video feeds from traffic cameras. Since this task requires a specialized AI service focused on image and video analysis, they create a single-service resource for Azure Computer Vision. This allows them to have granular control over the specific capabilities and configurations needed for traffic monitoring.

#### Multi-Service Example: Public Safety and Environmental Monitoring
For public safety and environmental monitoring, Innovaville needs to integrate multiple AI services. They plan to use:

- Azure Text Analytics to analyze social media posts and detect potential public safety threats.<br>
- Azure Speech Services to transcribe emergency calls and analyze the sentiment of callers.<br>
- Azure Anomaly Detector to monitor environmental sensors for unusual patterns in air quality and noise levels.

To streamline management and billing, Innovaville creates a multi-service resource. This allows them to access all these AI services with a single set of credentials and a unified endpoint, simplifying integration and reducing administrative overhead.

### Instructions for Flip Cards
Below are questions based on the scenario. Each question is on one side of a flip card. Flip the card to see the answer.

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
        <div class="tile" onclick="checkAnswer(this, 'Single-service account (Computer Vision)')">
            <div class="front">You need to analyze live video feeds from traffic cameras to monitor traffic flow and detect incidents in real-time. What type of Azure AI service account should you use?</div>
            <div class="back">Single-service account (Computer Vision)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Multi-service account (Language Service)')">
            <div class="front">Your project involves analyzing customer feedback from multiple sources, including social media, emails, and surveys, to understand sentiment and key topics. What type of Azure AI service account should you use?</div>
            <div class="back">Multi-service account (Language Service)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Multi-service account (Speech Services, Translator)')">
            <div class="front">You are developing a voice-activated virtual assistant that can understand and respond to user queries, transcribe spoken words, and translate languages. What type of Azure AI service account should you use?</div>
            <div class="back">Multi-service account (Speech Services, Translator)</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Single-service account')">
            <div class="front">Your team needs to use different tiers for different services and different members need different level of access for the services. What type of Azure AI service account should you use?</div>
            <div class="back">Single-service account</div>
        </div>
      
        <div class="tile" onclick="checkAnswer(this, 'Single-service account (Face API, Anomaly Detector, Language Service)')">
            <div class="front">You are tasked with creating a comprehensive security monitoring system that includes facial recognition for access control, anomaly detection for unusual activities, and text analysis for threat detection. What type of Azure AI service account should you use?</div>
            <div class="back">Single-service account (Face API, Anomaly Detector, Language Service)</div>
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
