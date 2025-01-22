---
layout: default
title:  "Storage Flip Card"
category: "Gamification"
sub-category: "Azure Infrastructure"
courses: [AZ-305,AZ-104, AZ-1003, AZ-204]
---

# Alex's Adventures in Azureland with Storage Account 

## Introduction

In the bustling city of Techville, two young tech enthusiasts, Alex and Zara, stumbled upon an ancient, mysterious book in their local library. The book, titled "The Secrets of Azureland," promised to unlock the hidden powers of the cloud.

Curious and excited, Alex and Zara decided to embark on a thrilling adventure to uncover these secrets. As they opened the book, a swirling vortex of light enveloped them, transporting them to a magical realm called Azureland.

In this enchanted land, their first mission was to uncover the secrets of Azure Storage. They were presented with several flip cards, each representing a unique feature of Azure Storage. Each card contained a question, and flipping the card would reveal the answer.

However, Alex and Zara were unfamiliar with Azure Storage Accounts. Your goal is to help them answer the questions correctly, collect all the cards, and become Azure Storage Masters!

<a href="./images/st1.png">
  <img src="./images/st1.png" alt="a boy and a girl reading a book">
</a>

### Instructions for Flip Cards
Below are questions based on the scenario. Each question is on one side of a flip card. Flip the card to see the answer.

<html lang="en">
<head>    
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
            background: linear-gradient(135deg, #d4f8e8, #66bb6a); 
              font-size: 20px;
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

        <div class="tile" onclick="checkAnswer(this, 'Read-access geo-redundant storage (RA-GRS) and Read-access geo-zone-redundant storage (RA-GZRS)')">
            <div class="front">Which redundancy options available for Azure Storage Accounts allows read access to the secondary region?</div>
            <div class="back">Read-access geo-redundant storage (RA-GRS) and Read-access geo-zone-redundant storage (RA-GZRS)</div>
        </div>

        <div class="tile" onclick="checkAnswer(this, 'Shared Access Signature')">
            <div class="front">Which Azure Blob access method allows providing access for a specific timespan?</div>
            <div class="back">Shared Access Signature</div>
        </div>

        <div class="tile" onclick="checkAnswer(this, 'Transaction Optimized Tier')">
            <div class="front">Which of these is NOT a security feature for Azure Storage Account?
            1. Shared Access Signatures (SAS)
            2. Azure Active Directory (Azure AD) Integration
            3. Encryption at Rest
            4. Transaction Optimized Tier
            5. Encryption in Transit
            </div>
            <div class="back">Transaction Optimized Tier</div>
        </div>

        <div class="tile" onclick="checkAnswer(this, 'Hot, Cool, Cold and Archive')">
            <div class="front">What are the different access tiers available for Azure Blob Storage?</div>
            <div class="back">Hot, Cool, Cold and Archive</div>
        </div>
      
        <div class="tile" onclick="checkAnswer(this, 'SMB and NFS')">
            <div class="front">Which protocols are supported by Azure File Share?</div>
            <div class="back">SMB and NFS</div>
        </div>

        <div class="tile" onclick="checkAnswer(this, 'Premium Performance Tier')">
        <div class="front">Which performance tier in Storage Account is suited for hosting data for a Mission Critical Application?</div>
        <div class="back">Premium Performance Tier!
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
                tile.querySelector('.back').style.backgroundColor = 'lightgray';
                tile.querySelector('.back').textContent = answer;
                tile.classList.add('flipped');
            }
        }
    </script>
