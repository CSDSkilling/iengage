---
layout: default
title:  "Why Microsoft Fabric"
category: "Comic"
sub-category: "Data and AI"
courses: [DP-203]
---

# Why Microsoft Fabric

## Introduction
This image is a comic-style illustration depicting a business meeting where team members are discussing their next "Digital Transformation Plan." The conversation revolves around selecting an appropriate platform that can handle data cleaning, storage, and analysis. The team considers various options and ultimately decides on Microsoft Fabric as the solution that meets their needs.
<a href="./images/f1.png" download>
  <img src="./images/f1.png" alt="A group of four people in a business meeting discussing">
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
