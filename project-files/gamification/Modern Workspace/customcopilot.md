---
layout: default
title:  "Copilot Studio Vs AI Foundry"
category: "Gamification"
sub-category: "Modern Workplace"
courses: [AI-3018, MS-4010]
---

# Copilot Studio Vs AI Foundry

## Introduction

Welcome to our exciting gamified learning experience! In this video, you'll join Helen and Alice as they discuss the differences between Copilot Studio and AI Studio. Pay close attention, because after their conversation, you'll have the chance to answer some questions and earn rewards!

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Modern Workspace/videos/customcopilot/customcopilot.mp4?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>


### Question 1:
**Your organization is planning to implement AI solutions to boost employee productivity. The management wants to automate tasks like drafting documents, summarizing emails, and generating reports directly within existing tools like Word and Excel, without building custom integrations or requiring developers to intervene. Additionally, the solution must cater to the entire organization, scaling across departments seamlessly. What would be the most appropriate solution for this scenario?**

<form id="quizForm1">
  <input type="radio" id="q1a" name="q1" value="A">
  <label for="q1a">A. Use Microsoft 365 Copilot to embed AI capabilities directly into existing tools for organization-wide productivity gains.</label><br>
  <input type="radio" id="q1b" name="q1" value="B">
  <label for="q1b">B. Implement Role-aligned Copilots to address department-specific use cases like security or sales.</label><br>
  <input type="radio" id="q1c" name="q1" value="C">
  <label for="q1c">C. Develop custom AI solutions using Azure AI Foundry to integrate advanced capabilities into Microsoft 365 apps.</label><br>
  <input type="radio" id="q1d" name="q1" value="D">
  <label for="q1d">D. Build and train AI agents in Copilot Studio and deploy them for document and email automation.</label><br>
  <button type="button" onclick="checkAnswer1()" class="styled-button">Submit</button>
</form>

<p id="result1"></p>

### Question 2:
**A startup specializing in customer service automation wants to streamline how they create and deploy virtual agents to handle common queries. They require a solution that allows them to build agents with natural language capabilities without worrying about managing infrastructure or multiple subscriptions. The system should also allow them to test and deploy agents quickly to adapt to customer needs. Which option would fulfill all these requirements?**

<form id="quizForm2">
  <input type="radio" id="q2a" name="q2" value="A">
  <label for="q2a">A. Utilize Copilot Studio to build, test, and deploy AI-powered agents through a simplified SaaS platform.</label><br>
  <input type="radio" id="q2b" name="q2" value="B">
  <label for="q2b">B. Deploy Microsoft 365 Copilot to handle customer service automation and integrate it into their CRM.</label><br>
  <input type="radio" id="q2c" name="q2" value="C">
  <label for="q2c">C. Leverage Azure OpenAI services to build custom APIs and handle natural language processing.</label><br>
  <input type="radio" id="q2d" name="q2" value="D">
  <label for="q2d">D. Use Role-aligned Copilots to deploy agents for customer service in specific roles like sales or finance.</label><br>
  <button type="button" onclick="checkAnswer2()" class="styled-button">Submit</button>
</form>

<p id="result2"></p>

### Question 3:
**You are a developer in an enterprise that already uses Microsoft 365 Copilot. Your team needs to enhance Copilot's functionality by adding custom knowledge about your company’s products and integrating it with existing CRM systems. Which tool would you choose?**

<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A. Copilot Studio</label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B. Extensibility tools for Microsoft 365 Copilot</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C. Role-aligned Copilots</label><br>
  <input type="radio" id="q3d" name="q3" value="D">
  <label for="q3d">D. Azure AI Foundry</label><br>
  <button type="button" onclick="checkAnswer3()" class="styled-button">Submit</button>
</form>

<p id="result3"></p>

### Question 4:
**A tech company is developing a new application that requires advanced natural language processing, image generation, and speech-to-text capabilities. They want full access to pre-trained models like GPT, DALL-E, and Whisper via REST APIs to integrate these functionalities into their custom software. The company also needs flexibility to fine-tune models and implement specific use cases such as content moderation and custom chatbot development. Which solution should they choose?**

<form id="quizForm4">
  <input type="radio" id="q4a" name="q4" value="A">
  <label for="q4a">A. Azure AI Foundry</label><br>
  <input type="radio" id="q4b" name="q4" value="B">
  <label for="q4b">B. Azure OpenAI</label><br>
  <input type="radio" id="q4c" name="q4" value="C">
  <label for="q4c">C. Copilot Studio</label><br>
  <input type="radio" id="q4d" name="q4" value="D">
  <label for="q4d">D. Extensibility tools for Microsoft 365 Copilot</label><br>
  <button type="button" onclick="checkAnswer4()" class="styled-button">Submit</button>
</form>

<p id="result4"></p>

<script>
  function checkAnswer1() {
    var radios = document.getElementsByName('q1');
    var correctAnswer = 'A';
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
    var correctAnswer = 'A';
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

  function checkAnswer4() {
    var radios = document.getElementsByName('q4');
    var correctAnswer = 'B';
    var result = document.getElementById('result4');
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
