---
layout: default
title:  "Analytics with Power BI"
category: "Case Study"
sub-category: "Data and AI"
courses: [PL-300, DP-605, BL-PR-802]
---
# Empowering Banking Analytics with Power BI: A Contoso Bank Transformation

## Introduction
In the city of Seattle, Contoso Bank, a leading institution, is undertaking a transformative project to enhance its customer engagement and operational efficiency.

<a href="./images/pb1.png">
  <img src="./images/pb1.png" alt="man analysing the reports" class="img-fluid">
</a>

Their CTO has tasked the analytics team with designing an advanced reporting system using Microsoft Power BI to address the following requirements:

#### Requirement 1: Get Data
The team needs to connect to a highly scalable, NoSQL database containing real-time customer transaction data and account details. This data is stored in Azure Cosmos DB, and the team wants to bring it into Power BI for further analysis.

#### Requirement 2: Power Query editor
The analytics team wants to extract key insights from unstructured text data, such as customer feedback and complaint logs. They aim to identify recurring themes and sentiments to better understand customer needs and areas for improvement.

#### Requirement 3: Data Model
To enhance the analytical capabilities of their reports, the team needs to define and manage custom calculations across multiple measures, allowing users to switch between perspectives such as year-over-year growth or rolling averages seamlessly.

#### Requirement 4: Create Report
The team requires a visual representation of key performance indicators (KPIs) that go beyond the default options in Power BI. They plan to use a specialized visual to present data interactively and effectively.

#### Requirement 4: Power BI Service
Once the report is finalized, the team wants to securely share it with branch managers and executive stakeholders. They aim to create a centralized location where users can easily access and explore the report.


#### Match the correct answer to each question below by dragging and dropping.

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
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
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azureDataFabrics">Azure CosmosDB Connector</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azureSynapse">Text Analytics ( AI Insights)</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="crmSocialSales">Calculation Group</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="azurePurview">Microsoft Appsource</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="synapseSpark">Apps</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="synapseSpark1">AI Language Service</div>
    </div>
    <div>
        <p>Which Microsoft PowerBI functionality should be used for Requirement 1?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azureDataFabrics"></div>
    </div>
    <div>
        <p>Which Microsoft PowerBI functionality should be used for Requirement 2?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azureSynapse"></div>
    </div>
    <div>
        <p>Which Microsoft PowerBI functionality should be used for Requirement 3?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="crmSocialSales"></div>
    </div>
    <div>
        <p>Which Microsoft PowerBI functionality should be used for Requirement 4?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="azurePurview"></div>
    </div>
     <div>
        <p>Which Microsoft PowerBI functionality should be used for Requirement 5?</p>
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
