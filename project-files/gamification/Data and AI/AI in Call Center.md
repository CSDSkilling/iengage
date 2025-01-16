---
layout: default
title:  "AI Service in Call Center"
category: "Gamification1"
sub-category: "Data and AI"
courses: [AI-102]
---

# Multilingual Customer Support

## Introduction:

This is a dialog between Hiroshi and Amanda. Amanda works for a call center that handles customer inquiries from around the world. To provide efficient and personalized support, they leverage AI services.<br>
**Situation:** A customer from Japan calls the support line to inquire about a recent order. The customer speaks only Japanese, while the available support agent speaks only English.

## Task 1: Listen to the conversation between Hiroshi and Amanda

<a href="./images/cc.png">
  <img src="./images/cc.png" alt="Amanda talking to Hiroshi over the phone">
</a>
<br>
<audio controls>
  <source src=" /iengage/project-files/gamification/Data and AI/videos/callcenter.m4a" type="audio/mpeg"> 
  Your browser does not support the audio element.
</audio>

**Question 1** Which AI service enabled Amanda to respond to Hiroshi, even though she didn't speak Japanese?

 <div class="button-container">
    <button id="a1">Detect Language</button>
    <button id="a2" onclick="markCorrect()">Speech Translation</button>
    <button id="a3">Translate Service</button>
</div>
<p id="result"></p>

## Task 2: 

<style>
    .button-container {
        display: flex;
        gap: 10px;
    }
    .correct {
        background-color: green;
        color: white;
    }
</style>
<script>
    function markCorrect() {
        const button3 = document.getElementById('a2');
        button3.classList.add('correct');
        document.getElementById('result').innerText = 'Correct Answer';
    }
</script>