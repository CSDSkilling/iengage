---
layout: default
title:  "Service Endpoint Vs Private Endpoint"
category: "Gamification"
sub-category: "Azure Infrastructure"
courses: [AZ-500, AZ-104, AZ-700, AZ-305, AZ-1002]
---
# Fortify Lamna Healthcare's Data

## Introduction

Once upon a time in the bustling city of Techville, there was a renowned healthcare organization called Lamna Healthcare. 
Lamna Healthcare was known for its cutting-edge medical research and exceptional patient care. However, as the organization grew, so did its data security concerns. They needed to ensure that their patient data, stored in Azure SQL Database, was accessed privately and securely, without exposure to the public internet.

The IT team at Lamna Healthcare, led by the brilliant and meticulous Sarah, was tasked with finding a solution. Sarah knew that the stakes were high; patient data was sensitive and needed the highest level of protection. She gathered her team for a brainstorming session to evaluate their options.

## Match the features to each rows below by dragging and dropping.

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drag and Drop Text Example</title>
    <style>

        .draggable-text {
            display: inline-block;
            margin: 10px;
            padding: 10px 20px;
            border: 2px solid #ccc;
            border-radius: 5px;
            background-color: #fff;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, transform 0.3s;
        }
        .draggable-text:hover {
            background-color: #e0e0e0;
            transform: scale(1.05);
        }
        .drop-area {
            width: 300px;
            height: 50px;
            border: 2px dashed #ccc;
            border-radius: 5px;
            margin: 10px;
            display: inline-block;
            vertical-align: top;
            background-color: #fafafa;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, border-color 0.3s;
        }
        .drop-area:hover {
            background-color: #f0f0f0;
            border-color: #bbb;
        }
        .drop-area.correct {
            background-color: #d4edda;
            border-color: #c3e6cb;
        }
        .drop-area.incorrect {
            background-color: #f8d7da;
            border-color: #f5c6cb;
        }
        #message {
            font-size: 1.2em;
            margin-top: 20px;
            padding: 10px;
            border-radius: 5px;
            display: inline-block;
        }
    #message.correct {
            color: #155724;
            background-color: #d4edda;
            border: 1px solid #c3e6cb;
    }
    #message.incorrect {
            color: #721c24;
            background-color: #f8d7da;
            border: 1px solid #f5c6cb;
    }

     .drop-area-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px; /* Adjust the gap between the blocks as needed */
    }
    </style>
</head>
<body>
    <div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="1">Does not natively support cross-tenant connectivity</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="2">Connect to services across different Microsoft Entra tenants</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="3">Supports a wide range of Azure services</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="4">Supports fewer Azure services</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="5">Expensive solution due to the additional infrastructurerequired</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="6">Free of costU</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="7">Maps to a single resource</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="8">Provide access to multiple instances of a service</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="9">Uses a private IP address from your virtual network to connect to Azure service</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="10">Routes traffic through the Azure backbone network, but uses public IP address of the Azure service</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="11">Uses public DNS names to resolve the service's public IP address</div>
         <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="12">Uses private DNS zones to resolve the private IP address of the service</div>
    </div>

    <div>
        <p><b>Service Endpoint</b></p>
        <div class="drop-area-container">
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="1,4,6,8,10,11"></div>
          </div>
        <p class="message"></p>
    </div>

    <div>
        <p><b>Private Endpoint</b></p>
         <div class="drop-area-container">
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>        
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="2,3,5,7,9,12"></div>        
        </div>
        <p class="message"></p>
    </div>


    <script>
        function allowDrop(event) {
            event.preventDefault();
        }

        function drag(event) {
            event.dataTransfer.setData("text", event.target.id);
        }


    function drop(event) {
    event.preventDefault();
    var data = event.dataTransfer.getData("text");
    var draggedElement = document.getElementById(data);
    var dropAreaAnswers = event.target.getAttribute("data-answer").split(",");
    var messageElement = event.target.closest('div').querySelector('.message');

    if (event.target.children.length === 0) {
        if (dropAreaAnswers.includes(draggedElement.id)) {
            event.target.appendChild(draggedElement);
            event.target.classList.add("correct");
            event.target.classList.remove("incorrect");
            messageElement.innerText = "Correct!";
            messageElement.classList.add("correct");
            messageElement.classList.remove("incorrect");
        } else {
            event.target.classList.add("incorrect");
            event.target.classList.remove("correct");
            messageElement.innerText = "Error: Incorrect match.";
            messageElement.classList.add("incorrect");
            messageElement.classList.remove("correct");
        }
    } else {
        alert("This drop area is already occupied.");
    }
}

    </script>
</body>
