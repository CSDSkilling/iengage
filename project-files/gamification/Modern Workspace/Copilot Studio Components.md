---
layout: default
title:  "Copilot Studio-Actions and Components"
category: "Gamification"
sub-category: "Modern Workplace"
courses: [MS-4010, MS-4015]
---


# Understanding Key Actions and Components in Microsoft Copilot Studio

## Introduction

Welcome to the Microsoft Copilot Studio Drag-and-Drop Activity! This activity is designed to help you understand when to use various actions and components in Microsoft Copilot Studio, such as Conversation Actions, Prompt Actions, Flow Actions, Connectors, Topics, Variables, and Entities. By completing this activity, you'll gain a better understanding of how to build effective and interactive bots.
<a href="./images/pb1.png">
  <img src="./images/cb1.png" alt="man working with his laptop" class="img-fluid">
</a>

### Instructions

1. **Read Each Scenario:** Carefully read each scenario provided. Each scenario describes a specific situation or requirement in building a bot.
2. **Choose the Correct Action:** For each scenario, select the most appropriate action or component from the given options. The options include Conversation Action, Prompt Action, Flow Action, Connector, Topics, Variables, and Entities.
3. **Drag and Drop:** If this is a physical or digital drag-and-drop activity, drag the correct answer to the designated area for each question.
4. **Check Your Answers:** After completing all the scenarios, review your answers to ensure they are correct. You can compare your answers with the provided solutions to see how well you did.
5. **Learn and Reflect:** Take note of any mistakes and understand why the correct answer is the best choice for each scenario. This will help reinforce your learning and improve your skills in using Microsoft Copilot Studio.

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
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="conversation">Conversation action</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="entities">Entities</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="variables">Variable</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="connector">Connector</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="prompt">Prompt action</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="flow">Flow action</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="topics">Topics</div>
    </div>
    <div>
        <p>If you are creating a customer support bot to ask the user for their issue, provide troubleshooting steps, and confirm if the issue is resolved, what action can you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="conversation"></div>
    </div>
    <div>
        <p>After identifying the user's issue in a customer support bot, you need to ask for additional details like the product model and purchase date. What action can you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="prompt"></div>
    </div>
    <div>
        <p>Once you have collected all necessary details from the user, you want to automatically create a support ticket and send a confirmation email. What action can you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="flow"></div>
    </div>
    <div>
        <p>To fetch the user's order history from an external database and display it in the conversation, what action can you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="connector"></div>
    </div>
     <div>
        <p>If the user has multiple issues, such as billing inquiries and technical support, and you want to handle each issue separately, what should you create?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="topics"></div>
    </div>
     <div>
        <p>If you ask the user for their name and issue at the beginning of the interaction and want to use this information throughout the conversation, what should you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="variables"></div>
    </div>  
    <div>
        <p>If you need to extract specific information like product names, dates, and order numbers from the user's messages, what should you use?</p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="entities"></div>
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
