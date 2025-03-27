---
layout: default
title:  "Quest with AI Vision"
category: "Gamification"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3004]
---
# Quest with AI Vision

## Introduction

Meet Alex, a tech-savvy hero who loves solving problems with cutting-edge technology. Alex is on a mission to help the city of Techville, which is facing various challenges that can be solved using Azure AI Vision Service. Alex is joined by a team of sidekicks, each representing a feature of Azure AI Vision Service:

**OCR Owl:** A wise owl who can read and extract text from any image.<br>
**Tagging Tiger:** A fierce tiger who can identify and tag objects in images.<br>
**Face Falcon:** A sharp-eyed falcon who can detect and analyze faces.<br>
**Analyze Ant:** A diligent ant who can analyze image content and provide insights.

<a href="./images/av1.png">
  <img src="./images/av1.png" alt="Alex is joined by a team of sidekicks" class="img-fluid">
</a>
<br>

The city is threatened by a group of villains, each representing a challenge:

**Blurry Bandit:** Causes images to be blurry and hard to analyze.<br>
**Shadow Shifter:** Creates shadows that obscure important details in images.<br>
**Noise Nuisance:** Adds random noise to images, making them difficult to process.<br>
**Distortion Demon:** Warps images, making it hard to recognize objects.<br>

<a href="./images/av2.png">
  <img src="./images/av2.png" alt="a group of villains" class="img-fluid">
</a>
<br>

### First Challenge: The Blurry Bandit
Alex and OCR Owl encounter their first challenge.

**Which Azure AI Vision Service feature did OCR Owl use to extract the text from the blurry images**

<form id="quizForm1">
  <input type="radio" id="q1a" name="q1" value="A">
  <label for="q1a">A. Image Tagging</label><br>
  <input type="radio" id="q1b" name="q1" value="B">
  <label for="q1b">B. Face Detection</label><br>
  <input type="radio" id="q1c" name="q1" value="C">
  <label for="q1c">C. Optical Character Recognition (OCR)</label><br>
  <input type="radio" id="q1d" name="q1" value="D">
  <label for="q1d">D. Image Analysis</label><br>
  <button type="button" onclick="checkAnswer1()" class="styled-button">Submit</button>
</form>

<p id="result1"></p>

### Second Challenge: The Shadow Shifter
Next, Alex and Tagging Tiger face the Shadow Shifter, who has cast shadows over surveillance footage. 

**How did Tagging Tiger identify objects in shadowy images?**

<form id="quizForm2">
  <input type="radio" id="q2a" name="q2" value="A">
  <label for="q2a">A. Face Detection</label><br>
  <input type="radio" id="q2b" name="q2" value="B">
  <label for="q2b">B. Image Tagging</label><br>
  <input type="radio" id="q2c" name="q2" value="C">
  <label for="q2c">C. Text Extraction</label><br>
  <input type="radio" id="q2d" name="q2" value="D">
  <label for="q2d">D. Image Analysis</label><br>
  <button type="button" onclick="checkAnswer2()" class="styled-button">Submit</button>
</form>

<p id="result2"></p>

### Final Challenge: The Distortion Demon
In the final showdown, Alex and the team confront the Distortion Demon, who has warped images of missing persons. Face Falcon uses its face detection and analysis powers to recognize and analyze the faces, helping to locate the missing individuals.

**Which feature did Face Falcon use to recognize and analyze faces helping to locate the missing individuals?**

<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A. Image Tagging</label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B. Face Detection</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C. Optical Character Recognition (OCR)</label><br>
  <input type="radio" id="q3d" name="q3" value="D">
  <label for="q3d">D. Image Analysis</label><br>
  <button type="button" onclick="checkAnswer3()" class="styled-button">Submit</button>
</form>

<p id="result3"></p>


<script>
  function checkAnswer1() {
    var radios = document.getElementsByName('q1');
    var correctAnswer = 'C';
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
    var correctAnswer = 'B';
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
