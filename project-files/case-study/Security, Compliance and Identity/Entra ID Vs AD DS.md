---
layout: default
title:  "ADDS vs Entra ID"
category: "Case Study"
sub-category: "Security, Compliance and Identity"
courses: [SC-200,SC-300, AZ-500]
---
# VanArsdel's Journey to Microsoft Entra ID

## Introduction:

VanArsdel Ltd, a mid-sized technology company, had been thriving for years with its robust on-premises infrastructure. The company's IT environment was managed by a dedicated team led by the experienced IT manager, Raj. VanArsdel Ltd. relied heavily on its on-premises Active Directory (ADDS) to manage user identities, access control, and resources within the company's network.
VanArsdel's on-premises ADDS was the backbone of its IT operations. It provided a secure and controlled environment where user accounts, computers, and other resources were managed centrally. Raj and his team of IT administrators used Domain Controllers to enforce security policies, manage user authentication, and ensure that only authorized personnel could access sensitive data. The system worked well, but it required significant maintenance, regular updates, and physical infrastructure to keep everything running smoothly.
As the company grew, they faced new challenges. Employees started working remotely more frequently, and the demand for cloud-based applications and services increased. Raj realized that the traditional on-premises ADDS setup was becoming a bottleneck, limiting the company's ability to adapt to the changing work environment.
To address these challenges, they decided to explore Microsoft Entra ID. Raj and his team began the gathering the details for migration process, integrating Microsoft Entra ID with their existing on-premises ADDS to create a hybrid environment, leveraging  the strengths of both systems.

Your goal is to help the team identify which features or services belong to ADDS and which ones belong to Microsoft Entra ID. 


## Match the features to each column below by dragging and dropping.
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
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Kerberos/NTLM">Kerberos, NTLM</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="SAML/OIDC/ WS-FED">SAML, OIDC, WS-FED</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Tenants">Tenants</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="On-premises Printers">On-premises Printers</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="M365 and Azure Services integration">M365 and Azure Services integration</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Forest/Domain/OU">Forest, Domain, OU</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Cloud Identity">Cloud Identity</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Policy">Group Policy</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="CPolicy">Conditional Access Policy</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="On-premises identity">On-premises Identity</div>
        <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="On-premises application">On-premises application</div>

         <div class="draggable-text" draggable="true" ondragstart="drag(event)" id="Policy2" style="display: none;">Policy</div>
    </div>
    <div>
        <p><b>Entra ID</b></p>
        <div class="drop-area-container">
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="SAML/OIDC/ WS-FED,Tenants,M365 and Azure Services integration,Cloud Identity,CPolicy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="SAML/OIDC/ WS-FED,Tenants,M365 and Azure Services integration,Cloud Identity,CPolicy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="SAML/OIDC/ WS-FED,Tenants,M365 and Azure Services integration,Cloud Identity,CPolicy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="SAML/OIDC/ WS-FED,Tenants,M365 and Azure Services integration,Cloud Identity,CPolicy"></div>
          <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="SAML/OIDC/ WS-FED,Tenants,M365 and Azure Services integration,Cloud Identity,CPolicy"></div>
          </div>
        <p class="message"></p>
    </div>

    <div>
        <p><b>Active Directory Domain Services</b></p>
         <div class="drop-area-container">
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>        
        <div class="drop-area" ondrop="drop(event)" ondragover="allowDrop(event)" data-answer="Kerberos/NTLM,On-premises Printers,Forest/Domain/OU,On-premises identity,On-premises application,Policy"></div>        
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

