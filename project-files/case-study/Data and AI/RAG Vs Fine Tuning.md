---
layout: default
title:  " RAG Vs Fine Tuning"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3018, AI-3016]
---

# Enhancing a Customer Support Chatbot with RAG and Fine Tuning

## Introduction
In today's fast-paced digital world, customer support chatbots play a crucial role in providing timely and accurate assistance to users. However, as products and services evolve, these chatbots often struggle to keep up with the latest information and handle complex queries effectively. This case study explores the challenges faced by a customer support team and how they can leverage advanced AI techniques to improve their chatbot's performance.

## Scenario
Alex and Jamie, two colleagues working in the customer support department of a tech company, are tasked with enhancing their chatbot's capabilities. The chatbot has been underperforming, particularly with queries that require up-to-date information and a deep understanding of the company's products and services. Alex and Jamie are considering two AI techniques: Retrieval Augmented Generation (RAG) and fine-tuning, but they are unsure which one to use.

**Listen to the conversation between Alex and Jamie**

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/case-study/Data and AI/videos/rag-finetuning/rag-finetuning_player.html?embedIFrameId=embeddedSmartPlayerInstance" width="800" height="480" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

**Help Jamie to find answers for the below questions**

Below are questions based on the scenario. Help Jamie identify when to use RAG, fint-tuning and both
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
        <div class="tile" onclick="checkAnswer(this, ' RAG - Because the information is recent and needs to be retrieved from up-to-date sources.')">
            <div class="front">The chatbot needs to provide accurate responses about the latest software updates and features that were released last week. Which technique should be used?</div>
            <div class="back"> RAG - Because the information is recent and needs to be retrieved from up-to-date sources.</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'Fine-Tuning - Because the issues are consistent and can be addressed by training the model on a specific dataset.')">
            <div class="front">The chatbot frequently encounters queries about troubleshooting common issues with the company's products, which have been consistent over the past year.Which technique should be used?</div>
            <div class="back">Fine-Tuning - Because the issues are consistent and can be addressed by training the model on a specific dataset.</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'RAG - Because the policies are updated frequently, and the chatbot needs to access the latest information.')">
            <div class="front">The chatbot needs to answer questions about recent changes in company policies that are updated monthly.Which technique should be used?</div>
            <div class="back">RAG - Because the policies are updated frequently, and the chatbot needs to access the latest information.</div>
        </div>
        <div class="tile" onclick="checkAnswer(this, 'RAG and Fine-tuning - Because the chatbot needs to handle both consistent queries and the latest information, combining both techniques would be most effective.')">
            <div class="front">The chatbot is required to handle a wide range of customer queries, including both frequently asked questions and the latest product announcements. Which technique should be used?</div>
            <div class="back">RAG and Fine-tuning - Because the chatbot needs to handle both consistent queries and the latest information.</div>
        </div>
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
