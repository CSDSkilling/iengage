---
layout: default
title:  "Data Integration and Analysis -Synapse and Fabrics"
category: "Case Study"
sub-category: "Data and AI"
courses: [DP-203, DP-3012, DP-600, DP-700]
---
# Data Integration and Analysis with Azure Synapse Analytics and Microsoft Fabric

## Introduction
In the bustling city of Dataville, a team of data scientists at the company Contoso is on a mission to unlock the secrets of their vast data landscape. They have recently adopted Microsoft Fabrics to seamlessly integrate their diverse data sources and Azure Synapse Analytics to analyze and gain insights from their data.

One day, the team receives an urgent request from their CEO: they need to predict customer behavior for an upcoming product launch. The team springs into action, using Microsoft Fabric to connect data from their CRM, social media, and sales databases. With all the data unified, they turn to Azure Synapse Analytics to run complex queries and machine learning models.

As they delve deeper, they uncover patterns and trends that were previously hidden. The insights they gain not only help in predicting customer behavior but also reveal opportunities for new product features. The CEO is thrilled with the results, and the team celebrates their success, knowing they have mastered the art of data integration and analysis.

### Match the correct answer to each question below by dragging and dropping.

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
    </style>
</head>
<body>
    <div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azureDataFabrics">Microsoft Fabric</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azureSynapse">Azure Synapse Analytics</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="crmSocialSales">CRM,social media,sales</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azurePurview">Microsoft Purview</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="synapseSpark">Synapse Spark</div>
    </div>
    <div>
        <p>What platform did the team use to integrate diverse data sources and store the data in a Lakehouse?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azureDataFabrics"></div>
    </div>
    <div>
        <p>Which platform did the team use for data analysis and running machine learning models?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azureSynapse"></div>
    </div>
    <div>
        <p>What type of data sources were connected using Microsoft Fabric?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="crmSocialSales"></div>
    </div>
    <div>
        <p>What Azure service can be used to create a unified data governance solution across the organization?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azurePurview"></div>
    </div>
    <div>
        <p>Which feature of Azure Synapse Analytics allows for real-time data processing and analytics?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="synapseSpark"></div>
    </div>
    <p id="message"></p>

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
            var dropAreaAnswer = event.target.getAttribute("data-answer");

            if (draggedElement.id === dropAreaAnswer) {
                event.target.appendChild(draggedElement);
                event.target.classList.add("correct");
                event.target.classList.remove("incorrect");
                var messageElement = document.getElementById("message");
                messageElement.innerText = "Correct!";
                messageElement.classList.add("correct");
                messageElement.classList.remove("incorrect");
            } else {
                event.target.classList.add("incorrect");
                event.target.classList.remove("correct");
                var messageElement = document.getElementById("message");
                messageElement.innerText = "Error: Incorrect match.";
                messageElement.classList.add("incorrect");
                messageElement.classList.remove("correct");
            }
        }
    </script>
</body>
</html>
