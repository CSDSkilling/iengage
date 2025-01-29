---
layout: default
title:  "APIM in banking"
category: "Comic"
sub-category: "Digital and App Innovation"
courses: [AZ-204,AZ-305]
---
# API Management in banking

## Introduction
In this conversation, a developer and an architect discuss how the Contoso Bank leveraged Microsoft Azure and Azure API Management (APIM) to handle rapid growth and enhance their banking services. They explore the benefits of APIM in improving transaction security, speed, and customer experience, highlighting its impact on both mobile and corporate banking platforms.

<a href="./images/apim1.jpg" download>
  <img src="./images/apim1.jpg" alt=" four-panel comic strip showing two business professionals discussing Contoso Bank's growth and transformation. They mention the significant increase in users and transactions, the role of Azure API Management (APIM) in enhancing digital banking services, the launch of a new Corporate Internet Banking platform, and the overall improvement in operations through Azure services">
</a>

<a href="./images/apim2.jpg" download>
  <img src="./images/apim2.jpg" alt="A two-panel comic strip featuring a conversation between two business professionals. In the first panel, they discuss the significant improvement in customer experience at Contoso Bank, highlighting how opening a new bank account and issuing credit cards now take just minutes. In the second panel, they emphasize the role of Azure API Management (APIM) and Azure services in ensuring service availability, reliability, and supporting seamless and secure transactions for Contoso's clients in the UAE">
</a>

## Knowledge Check

What were the key benefits Contoso Bank experienced by implementing Azure API Management (APIM) and Entra ID?

<form id="quizForm">
  <input type="radio" id="q1" name="answer" value="q1">
  <label for="a1"> Improved security and speed, efficient API management, and quick partner onboarding.</label><br>
  <input type="radio" id="q2" name="answer" value="q2">
  <label for="a2">Reduced client base, slower infrastructure, and manual processes.</label><br>
  <input type="radio" id="q3" name="answer" value="q3">
  <label for="a3">Increased manual processes, decreased security, and slower partner onboarding.</label><br>
  <input type="radio" id="q4" name="answer" value="q4">
  <label for="a4">No significant changes in operations or security.</label><br>
  <button type="button" onclick="checkAnswer()" class="styled-button">Submit</button>
</form>

<p id="result"></p>

<script>
  function checkAnswer() {
    var radios = document.getElementsByName('answer');
    var correctAnswer = 'q1';
    var result = document.getElementById('result');
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
