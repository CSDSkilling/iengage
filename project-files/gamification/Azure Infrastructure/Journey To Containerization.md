---
layout: default
title:  "Journey to Containerization"
category: "Gamification"
sub-category: "Azure Infrastructure"
courses: [AZ-104,AZ-204,AZ-2003]
---

# ACR: Journey to Containerization

## Introduction:

Welcome to the world of TechWave Solutions, a dynamic and innovative company that has been at the forefront of technological advancements for over a decade. TechWave Solutions specializes in developing cutting-edge software applications that cater to a diverse range of industries, from healthcare to finance. As the demand for scalable and efficient solutions continues to grow, TechWave Solutions has decided to embark on a transformative journey to modernize their application infrastructure.
The company has recognized the immense potential of containerization in streamlining their development and deployment processes. By leveraging Docker and Azure Container Registry, TechWave Solutions aims to enhance the portability, security, and scalability of their applications. This transformation will not only improve their operational efficiency but also enable them to deliver high-quality solutions to their clients with greater speed and reliability.
In this activity, you will step into the shoes of TechWave Solutions' development team. Your mission is to create a Docker file, build the image, and push it to the Azure Container Registry. 

## Scenario: 

You are a developer tasked with containerizing your Python app and run it. Your app code is present in ‘sample.py’ present in your local machine. Use the instructions given and arrange them in order to complete the task given to you on the right-hand side.


**Question 1: Rearrange the following instructions and create a functional Docker file for the python application that you are developing. Dockerfile Instructions:**


<ul id="sortable-setup" class="styled-list">
  <li class="ui-state-default" data-order="4">WORKDIR.</li>
  <li class="ui-state-default" data-order="6">CMD [“python”, “sample.py”]</li>
  <li class="ui-state-default" data-order="5">COPY sample.py .</li>
  <li class="ui-state-default" data-order="2">Run apt-get update && apt-get install -y</li>
  <li class="ui-state-default" data-order="3">RUN mkdir /app</li>
  <li class="ui-state-default" data-order="1">FROM python</li>
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

## Question 2: 


Now since you got the Dockerfile now, you are ready to build the container image and push it to the container registry. We will be using Azure Container Registry (ACR) for hosting our container images. Please select what tools you can use to build your image and push it to ACR. Choose all that apply.

<form id="quiz-form">
  <label class="checkbox-container"><input type="checkbox" name="service" value="1"> A. Docker CLI<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="2"> B. Azure ACR Tasks<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="3"> C. Kubectl<span class="checkmark"></span></label><br>
  <label class="checkbox-container"><input type="checkbox" name="service" value="4">D. Azure CLI<span class="checkmark"></span></label><br>

  <button type="button" onclick="checkAnswers()">Check Answer</button>
  <button type="button" onclick="showAnswers()">Help Me</button>
</form>

<p id="result"></p>

<style>
 

  #result {
    font-size: 20px;
    margin-top: 20px;
  }

  #result.correct {
    color: blue;
  }

  #result.incorrect {
    color: red;
  }
</style>

<script>
  const correctAnswers = [1, 2];

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



## Question 3: 
Please select the right Azure ACR Task command to build the container image and push the image to ACR. Select one.

<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A) az acr build --registry $ACR_NAME --image <image-name>:v1 --file /path/to/Dockerfile /path/to/build/context</label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B) az build -–registry $ACR_Name –image  <image-name>:v1 Dockerfile</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C) acr build -–registry $ACR_Name –image  <image-name>:v1 Dockerfile</label><br>
  <input type="radio" id="q3d" name="q3" value="D">
  <label for="q3d">D) Azure AI Bot Service with QnA Maker </label><br>
  <button type="button" onclick="checkAnswer('q3', 'C', 'result3')" class="styled-button">Submit</button>
</form>

<p id="result3"></p>


<script>
   function checkAnswer3() {
    var radios = document.getElementsByName('q3');
    var correctAnswer = 'A';
    var result = document.getElementById('result3');
    var selected = false;

    for (var i = 0; i < radios.length; i++) {
      if (radios[i].checked) {
        selected = true;
        if (radios[i].value === correctAnswer) {
          result.textContent = 'Correct!';
          result.style.color = 'green';
        } else {
          result.textContent = 'Incorrect. Try again!';
          result.style.color = 'red';
        }
        break;
      }
    }

    if (!selected) {
      result.textContent = 'Please select an answer.';
      result.style.color = 'orange';
    }
  }

 
</script>
