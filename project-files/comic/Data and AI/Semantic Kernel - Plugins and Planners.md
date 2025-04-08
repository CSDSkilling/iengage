---
layout: default
title:  "Semantic Kernel - Plugins Vs Planners"
category: "Comic"
sub-category: "Data and AI"
courses: [AI-3018]
---

# Why Microsoft Fabric

## Introduction
This image is a comic-style illustration depicting a business meeting where team members are discussing their next "Digital Transformation Plan." The conversation revolves around selecting an appropriate platform that can handle data cleaning, storage, and analysis. The team considers various options and ultimately decides on Microsoft Fabric as the solution that meets their needs.
<a href="./images/sk1.PNG">
  <img src="./images/sk1.PNG" alt="A group of kids talking" class="img-fluid">
</a>

## Knowledge Check

Fabric is a new solution suitable for solving most data problems. Which of the following data tasks can Fabric perform?

<form id="quizForm">
  <input type="radio" id="q1" name="answer" value="q1">
  <label for="a1"> Data visualization</label><br>
  <input type="radio" id="q2" name="answer" value="q2">
  <label for="a2">Data analysis</label><br>
  <input type="radio" id="q3" name="answer" value="q3">
  <label for="a3">Data transformation</label><br>
  <input type="radio" id="q4" name="answer" value="q4">
  <label for="a4">All of the above</label><br>
  <button type="button" onclick="checkAnswer()" class="styled-button">Submit</button>
</form>

<p id="result"></p>

<script>
  function checkAnswer() {
    var radios = document.getElementsByName('answer');
    var correctAnswer = 'q4';
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
