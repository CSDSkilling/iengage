---
layout: default
title:  "Onboarding Avatar"
category: "Gamification"
sub-category: "Data and AI"
courses: [AI-102, AI-3003]
---

# TechNova’s AI Employee Onboarding Avatar

## Introduction

Welcome to TechNova, a leading innovator in the technology industry. At TechNova, we believe in harnessing the power of cutting-edge technology to create a seamless and efficient work environment for our employees. To ensure a smooth onboarding experience for our new hires, we have introduced Nova, our AI-powered onboarding avatar. Nova is designed to assist new employees in navigating the company's policies, processes, and resources, making their transition into the TechNova family as smooth as possible.
Meet John, a new employee who has just joined TechNova as a Software Engineer. On their first day, John is introduced to Nova, the AI onboarding avatar. Nova greets John with a warm welcome and offers to guide them through the onboarding process.

## Video
This video contains discussion about Service Endpoint and Private Endpoint. Watch the video and participate in the activity below to reinforce your learning.


By the end of the day, John feels confident and well-informed, thanks to Nova's guidance. They are now ready to embark on their journey at TechNova, knowing that they have a reliable AI Avatar to support them every step of the way.

## Activity

**Question 1:** Which Azure AI service was used to create the AI-powered onboarding avatar, Nova?
<form id="quizForm1">
  <input type="radio" id="q1a" name="q1" value="A">
  <label for="q1a">A. Azure Machine Learning</label><br>
  <input type="radio" id="q1b" name="q1" value="B">
  <label for="q1b">B. Azure AI Speech Service</label><br>
  <input type="radio" id="q1c" name="q1" value="C">
  <label for="q1c">C. Azure Bot Service</label><br>
  <input type="radio" id="q1d" name="q1" value="D">
  <label for="q1d">D. Azure AI Language Services</label><br>
  <button type="button" onclick="checkAnswer1()" class="styled-button">Submit</button>
</form>

<p id="result1"></p>


**Question 2:** Which of the following is a key feature of Azure AI Speech service that can be utilized to create an AI-powered onboarding avatar like Nova?
<form id="quizForm2">
  <input type="radio" id="q2a" name="q2" value="A">
  <label for="q2a">A. Image recognition</label><br>
  <input type="radio" id="q2b" name="q2" value="B">
  <label for="q2b">B. Speech-to-text conversion</label><br>
  <input type="radio" id="q2c" name="q2" value="C">
  <label for="q2c">C. Data analysis</label><br>
  <input type="radio" id="q2d" name="q2" value="D">
  <label for="q2d">D. Cloud storage</label><br>
  <button type="button" onclick="checkAnswer2()" class="styled-button">Submit</button>
</form>

<p id="result2"></p>


**Question 3:** How can Azure AI Language service be used to enhance the conversational capabilities of an AI agent?
<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A. By providing weather updates</label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B. By translating text into multiple languages</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C. By analyzing sentiment and intent in text</label><br>
  <input type="radio" id="q3d" name="q3" value="D">
  <label for="q3d">D. By storing large amounts of data</label><br>
  <button type="button" onclick="checkAnswer3()" class="styled-button">Submit</button>
</form>

<p id="result3"></p>


<script>
  function checkAnswer1() {
    var radios = document.getElementsByName('q1');
    var correctAnswer = 'B';
    var result = document.getElementById('result1');
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

  function checkAnswer2() {
    var radios = document.getElementsByName('q2');
    var correctAnswer = 'B';
    var result = document.getElementById('result2');
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

  function checkAnswer3() {
    var radios = document.getElementsByName('q3');
    var correctAnswer = 'C';
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
