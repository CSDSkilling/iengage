---
layout: default
title:  "Microsoft Fabric in Healthcare"
category: "Comic"
sub-category: "Data and AI"
courses: [DP-203, DP-600, DP-601, DP-602, DP-603, DP-604]
---

# Microsoft Fabric in Healthcare

## Introduction
In this insightful comic, follow a team of dedicated professionals as they embark on a journey to revolutionize healthcare data integration using Microsoft Fabric. As they navigate the complexities of merging data from Electronic Health Records (EHRs) and wearable devices, they tackle challenges like ensuring data quality, compliance with HIPAA regulations, and leveraging serverless SQL pools for efficient data management. Join them in this engaging story to discover how modern technology can transform healthcare outcomes and streamline data processes.

<a href="./images/lh1.jpg" download>
  <img src="./images/lh1.jpg" alt="A four-panel comic strip featuring two business professionals discussing the integration of data into their workflow. They talk about using Microsoft Fabric's serverless SQL pools for analytics, integrating data from EHRs and wearables, ensuring data quality and consistency, and complying with regulations like HIPAA." class="img-fluid">
</a>

## Knowledge Check

What is the primary goal of the project discussed in the image?

<form id="quizForm">
  <input type="radio" id="q1" name="answer" value="q1">
  <label for="a1"> To improve data security</label><br>
  <input type="radio" id="q2" name="answer" value="q2">
  <label for="a2">To create a unified data platform for analytics</label><br>
  <input type="radio" id="q3" name="answer" value="q3">
  <label for="a3">To develop new wearable technology</label><br>
  <input type="radio" id="q4" name="answer" value="q4">
  <label for="a4">To enhance SQL query performance</label><br>
  <button type="button" onclick="checkAnswer()" class="styled-button">Submit</button>
</form>

<p id="result"></p>

<script>
  function checkAnswer() {
    var radios = document.getElementsByName('answer');
    var correctAnswer = 'q2';
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
