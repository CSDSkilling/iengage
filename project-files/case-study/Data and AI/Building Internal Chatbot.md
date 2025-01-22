---
layout: default
title:  "Building an Internal Chatbot"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, AI-3016, AI-3022, PR-801]
---

# Building an Internal Chatbot with Azure AI Services

## Introduction
Ben, an AI architect at a mid-sized company, is tasked with developing an internal chatbot to streamline access to corporate resources. These resources are currently dispersed across multiple knowledge bases and document repositories, making it challenging for employees to find the information they need quickly and efficiently.

<a href="./images/cb1.png">
  <img src="./images/cb1.png" alt="a group of people around a table with a robot">
</a>

### Objective
The primary goal is to create a chatbot that can connect employees with the necessary corporate resources, improving productivity and reducing the time spent searching for information.

<a href="./images/cb2.png" download>
  <img src="./images/cb2.png" alt="a close-up of highlighting different challenges - Dispersed Information, Security , Compliance and User Experience">
</a>

### Challenges
- Dispersed Information: Corporate resources are spread across various platforms, including SharePoint, OneDrive, and internal databases.
- User Experience: Employees need a user-friendly interface to interact with the chatbot.
- Security and Compliance: Ensuring that sensitive corporate information is accessed securely.

**Question 1:** To address the challenges of dispersed information, user experience, and security, which Azure services should Ben use? Select all that apply.
<form id="quiz-form">
  <label class="checkbox-container"><input type="checkbox" name="service" value="1"> Azure AI Cognitive Service Account<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="2"> Azure OpenAI Service<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="3"> Azure AI Search<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="4"> Azure AI Document Intelligence<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="5"> Azure AI Bot Service<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="6"> Private Endpoint<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="7"> Azure SQL Database<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="8"> Azure DevOps<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="9"> Azure Machine Learning<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="10"> Managed Identity<span class="checkmark"></span></label><br>
  <br>
  <button type="button" onclick="checkAnswers()">Check Answer</button>
  <button type="button" onclick="showAnswers()">Help Me</button>
</form>

<p id="result"></p>


<script>
  const correctAnswers = [2, 3, 5, 6, 10];

  function checkAnswers() {
    const selected = Array.from(document.querySelectorAll('input[name="service"]:checked')).map(cb => parseInt(cb.value));
    const isCorrect = correctAnswers.every(val => selected.includes(val)) && selected.length === correctAnswers.length;
    const resultElement = document.getElementById('result');
    resultElement.innerText = isCorrect ? 'Correct' : 'Try again';
    resultElement.className = isCorrect ? 'correct' : 'incorrect';
  }

  function showAnswers() {
    document.querySelectorAll('input[name="service"]').forEach(cb => {
      cb.checked = correctAnswers.includes(parseInt(cb.value));
    });
    const resultElement = document.getElementById('result');
    resultElement.innerText = 'This is the correct order';
    resultElement.className = 'correct';
  }
</script>

**Question 2:** Below are the tasks involved in the implementation phase. They are currently out of order. Please reorder them correctly.

<ul id="sortable-setup" class="styled-list">
  <li class="ui-state-default" data-order="5">Testing and Deployment: The chatbot undergoes rigorous testing to ensure it meets user needs and performs reliably. It is then deployed within Microsoft Teams for easy access.</li>
  <li class="ui-state-default" data-order="3">Integration with Corporate Resources: The chatbot is connected to various knowledge bases and document repositories using APIs, ensuring it can retrieve and present information from multiple sources.</li>
  <li class="ui-state-default" data-order="1">Requirement Gathering: Ben's team conducts interviews with employees to understand their needs and the types of queries they typically have.</li>
  <li class="ui-state-default" data-order="6">Results: The outcomes of the implementation, such as improved efficiency and enhanced user experience.</li>
  <li class="ui-state-default" data-order="2">Design and Development: Using Azure AI Bot Service, the team designs the chatbot's conversational flow and integrates it with Azure OpenAI Service for natural language understanding.</li>
  <li class="ui-state-default" data-order="4">Grounding Responses: Ground the responses of Azure OpenAI Service to the corporate resources.</li>
</ul>

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>

<p id="feedback-setup"></p>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<script>
  $(function() {
    $("#sortable-setup").sortable();
    $("#sortable-setup").disableSelection();
  });

  function checkOrderSetup() {
    var items = $("#sortable-setup li");
    var correct = true;
    items.each(function(index) {
      if ($(this).data("order") !== index + 1) {
        correct = false;
      }
    });
    var feedback = document.getElementById("feedback-setup");
    if (correct) {
      feedback.textContent = "Correct order!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Incorrect order. Try again.";
      feedback.style.color = "red";
    }
  }

  function helpMeSetup() {
    var items = $("#sortable-setup li").sort(function(a, b) {
      return $(a).data("order") - $(b).data("order");
    });
    $("#sortable-setup").html(items);
    document.getElementById("feedback-setup").textContent = "Here is the correct order.";
    document.getElementById("feedback-setup").style.color = "blue";
  }
</script>

**Question 3:** In his presentation to key stakeholders, Ben aims to showcase the Azure services utilized to tackle these challenges and develop the chatbot. 

3a) What essential aspects of Azure AI Search service should he highlight ?

<form id="quiz-form-1">
  <label class="checkbox-container"><input type="checkbox" name="service1" value="1"> Efficient Query Processing<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service1" value="2"> Multiple Data Sources<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service1" value="3"> Limited to Azure SQL Database only<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service1" value="4"> Cognitive Skills<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service1" value="5"> Manual Indexing Required<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service1" value="6"> Full-Text Search<span class="checkmark"></span></label><br>
  <br>
  <button type="button" onclick="checkAnswers1()">Check Answer</button>
  <button type="button" onclick="showAnswers1()">Help Me</button>
</form>

<p id="result1"></p>


<script>
  const correctAnswers1 = [1, 2, 4, 6];

  function checkAnswers1() {
    const selected = Array.from(document.querySelectorAll('input[name="service1"]:checked')).map(cb => parseInt(cb.value));
    const isCorrect = correctAnswers1.every(val => selected.includes(val)) && selected.length === correctAnswers1.length;
    const resultElement = document.getElementById('result1');
    resultElement.innerText = isCorrect ? 'Correct' : 'Try again';
    resultElement.className = isCorrect ? 'correct' : 'incorrect';
  }

  function showAnswers1() {
    document.querySelectorAll('input[name="service1"]').forEach(cb => {
      cb.checked = correctAnswers1.includes(parseInt(cb.value));
    });
    const resultElement = document.getElementById('result1');
    resultElement.innerText = 'These are the right choices';
    resultElement.className = 'correct';
  }
</script>

3b) What essential aspects of Azure Open AI service should he highlight ? 

<form id="quiz-form-2">
  <label class="checkbox-container"><input type="checkbox" name="service2" value="1"> Diverse Models available<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service2" value="2"> Limited to text generation only<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service2" value="3"> Easily integrates with other Azure services like Azure AI Search<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service2" value="4"> Accessible through REST APIs and SDKs<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service2" value="5"> The responses are used to further train the Models<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service2" value="6"> Content Filtering protects against harmful output<span class="checkmark"></span></label><br>
  <br>
  <button type="button" onclick="checkAnswers2()">Check Answer</button>
  <button type="button" onclick="showAnswers2()">Help Me</button>
</form>

<p id="result2"></p>


<script>
  const correctAnswers2 = [1, 2, 4, 6];

  function checkAnswers2() {
    const selected = Array.from(document.querySelectorAll('input[name="service2"]:checked')).map(cb => parseInt(cb.value));
    const isCorrect = correctAnswers2.every(val => selected.includes(val)) && selected.length === correctAnswers2.length;
    const resultElement = document.getElementById('result2');
    resultElement.innerText = isCorrect ? 'Correct' : 'Try again';
    resultElement.className = isCorrect ? 'correct' : 'incorrect';
  }

  function showAnswers2() {
    document.querySelectorAll('input[name="service2"]').forEach(cb => {
      cb.checked = correctAnswers2.includes(parseInt(cb.value));
    });
    const resultElement = document.getElementById('result2');
    resultElement.innerText = 'These are the right choices';
    resultElement.className = 'correct';
  }
</script>
