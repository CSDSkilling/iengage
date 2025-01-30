---
layout: default
title:  " M365 Copilot Adoption"
category: "Case Study123"
sub-category: "Modern Workplace"

---


# Fabrikam’s Transformation: Microsoft 365 Copilot Adoption

In Latin America, Fabrikam, a mobility leader, undertook a project to boost customer engagement and efficiency by using Microsoft 365 Copilot.

## Challenge
Fabrikam aimed to enhance productivity, streamline operations, and promote inclusivity with the help of AI-driven solutions.

## Strategies for Adoption
- **User Enablement**: Empowered employees through targeted training, resources, and support to maximize AI’s potential.
- **Three-Part AI Approach**: Focused on leadership development, human transformation via robust enablement programs, and building technical skills.
- **People-First Strategy**: Emphasized human connection, leadership support, and emotional consideration during adoption.
- **Executive Alignment**: Clear vision and active support from leaders and peers ensured goal alignment and collaboration.
- **Copilot Center of Excellence (CoE)**: Fostered peer learning, rapid feedback, and a virtual community for sharing ideas and support.

## Key Successes
- **Productivity Boost**: Employees saved an average of 8.3 hours per month, with heavy users saving up to 25 hours, achieving a 10.6% productivity increase.
- **Operational Efficiency**: Tasks like customer feedback analysis and crisis response were completed in hours instead of days.
- **Inclusivity**: Real-time transcription and summaries enabled hearing-impaired employees to participate actively in meetings.
- **Crisis Management**: Streamlined emergency responses with Teams discussions and automated reports.

## Measuring Success
- Tracked KPIs and adoption metrics using the Copilot Dashboard.
- Conducted surveys and feedback sessions to gauge user satisfaction.
- Reviewed usage reports and held feedback campaigns for continuous improvement.

## Future Plans
Fabrikam aims to scale AI adoption with 42 use cases identified in pilots, expand Copilot use across departments, and explore tools like Microsoft Copilot for Finance.


## Map the case with the Microsoft 365 Copilot user enablement framework
<a href="./images/s1.png">
  <img src="./images/s1.png" alt="image of Copilot enablement framework">
</a>
<br>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Microsoft 365 Copilot Framework</title>
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
            width: 250px;
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
        .message {
            font-size: 1.2em;
            margin-top: 20px;
            padding: 10px;
            border-radius: 5px;
            display: inline-block;
        }
        .message.correct {
            color: #155724;
            background-color: #d4edda;
            border: 1px solid #c3e6cb;
        }
        .message.incorrect {
            color: #721c24;
            background-color: #f8d7da;
            border: 1px solid #f5c6cb;
        }
    </style>
</head>
<body>
    
    <!-- Draggable Items -->
    <div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="executive">Executive Alignment</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="three">Three-Part AI Approach</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="fut">Future Plans</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="user">User Enablement</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="meas">Measuring Success</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="copilot">Copilot Center of Excellence (CoE)</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="prod">Productivity Boost</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="oper">Operational Efficiency: </div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="people">People-First Strategy</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="incl">Inclusivity</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="crisis">Crisis Management</div>
    </div>

    <!-- Sections with Drop Areas -->
    <div>
        <p><b>Get Ready</b></p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="three,executive"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="three,executive"></div>
        
        <p class="message"></p>
    </div>

    <div>
        <p><b>Onboard and Engage</b></p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="user,people,copilot"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="user,people,copilot"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="user,people,copilot"></div>
        
        <p class="message"></p>
    </div>

    <div>
        <p><b>Deliver Impact</b></p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="prod,oper,incl,crisis"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="prod,oper,incl,crisis"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="prod,oper,incl,crisis"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="prod,oper,incl,crisis"></div>
        <p class="message"></p>
    </div>

    <div>
        <p><b>Extend and Optimize</b></p>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="meas,fut"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="meas,fut"></div>        
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
</html>
