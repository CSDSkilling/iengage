---
layout: default
title:  "Securing with Microsoft Defender"
category: "Case Study"
sub-category: "Security, Compliance and Identity"
courses: [SC-200]
---

# Contoso's Digital Transformation: Securing a Connected Future with Microsoft Defender and Advanced Security Solutions

## Introduction

Contoso, a global brewing company, has set an ambitious goal to become the best-connected brewer by digitalizing customer interactions and simplifying its IT landscape. With operations in over 80 countries, Contoso faces significant cybersecurity challenges due to the increasing threat landscape. To address these challenges, Contoso adopted a comprehensive security strategy, focusing on integrating advanced security tools and services.

The company transitioned from a fragmented and siloed security model to a seamless, integrated one. They adopted a hybrid security model, combining internal control with outsourced 24/7 security operations. Emphasizing Zero Trust principles, Contoso ensures continuous verification of identities to maintain a secure digital environment.
Contoso uses a variety of Microsoft Security solutions to protect its digital transformation efforts. Microsoft 365 E5 provides a comprehensive suite of advanced security features. The Microsoft Defender Suite, including Defender for Cloud, Defender for Cloud Apps, Defender for Endpoint, and Defender for Identity, offers protection for cloud environments, app usage, endpoints, and identities, respectively. Additionally, Microsoft Entra ID is used for identity and access management, while Microsoft Sentinel serves as the security information and event management (SIEM) tool for monitoring and response.
By leveraging these tools, Contoso has enhanced its security posture and agility, improved visibility and control over its IT environment, and ensured the ability to innovate securely while supporting global operations.


**Question 1**:<input type="text" id="cloudProtection" class="input-box" oninput="this.value = this.value.toUpperCase()"> is used for identity and access management.

<button type="button" onclick="checkAnswer1()">Check</button>
<button type="button" onclick="revealAnswer1()">Reveal Answer</button>

<p id="result"></p>

<script>
  function checkAnswer1() {
    var answer = document.getElementById('cloudProtection').value.toUpperCase();
    if (answer === 'MICROSOFT ENTRA ID') {
      document.getElementById('result').innerText = 'Correct answer';
    } else {
      document.getElementById('result').innerText = 'MICROSOFT ENTRA ID';
    }
  }

  function revealAnswer1() {
    document.getElementById('cloudProtection').value = 'MICROSOFT ENTRA ID';
    document.getElementById('result').innerText = '';
  }
</script>

**Question 2**:For security information and event management, Contoso uses Microsoft <input type="text" id="cloudProtection2" class="input-box" oninput="this.value = this.value.toUpperCase()"> 

<button type="button" onclick="checkAnswer2()">Check</button>
<button type="button" onclick="revealAnswer2()">Reveal Answer</button>

<p id="result2"></p>

<script>
  function checkAnswer2() {
    var answer = document.getElementById('cloudProtection2').value.toUpperCase();
    if (answer === 'SENTINEL') {
      document.getElementById('result2').innerText = 'Correct answer';
    } else {
      document.getElementById('result2').innerText = 'SENTINEL';
    }
  }

  function revealAnswer2() {
    document.getElementById('cloudProtection2').value = 'SENTINEL';
    document.getElementById('result2').innerText = '';
  }
</script>

**Question 3**:Contoso uses <select id="q1" onchange="checkAnswer('q1', 'DEFENDER FOR CLOUD')" class="styled-dropdown">
    <option value="">Select an answer</option>
    <option value="DEFENDER FOR CLOUD">Defender for Cloud</option>
    <option value="DEFENDER FOR CLOUD APPS">Defender for Cloud Apps</option>
    <option value="DEFENDER FOR ENDPOINT">Defender for Endpoint</option>
    <option value="DEFENDER FOR IDENTITY">Defender for Identity</option>
   </select> to protect its cloud environments.
   <span id="result1"></span>

**Question 3**:For securing app usage, Contoso relies on <select id="q2" onchange="checkAnswer('q2', 'DEFENDER FOR CLOUD APPS')" class="styled-dropdown">
    <option value="">Select an answer</option>
    <option value="DEFENDER FOR CLOUD">Defender for Cloud</option>
    <option value="DEFENDER FOR CLOUD APPS">Defender for Cloud Apps</option>
    <option value="DEFENDER FOR ENDPOINT">Defender for Endpoint</option>
    <option value="DEFENDER FOR IDENTITY">Defender for Identity</option>
   </select>.
   <span id="result2"></span>

**Question 3**:<select id="q3" onchange="checkAnswer('q3', 'DEFENDER FOR ENDPOINT')" class="styled-dropdown">
    <option value="">Select an answer</option>
    <option value="DEFENDER FOR CLOUD">Defender for Cloud</option>
    <option value="DEFENDER FOR CLOUD APPS">Defender for Cloud Apps</option>
    <option value="DEFENDER FOR ENDPOINT">Defender for Endpoint</option>
    <option value="DEFENDER FOR IDENTITY">Defender for Identity</option>
   </select> provides endpoint protection for HEINEKEN.
   <span id="result3"></span>

**Question 3**:To monitor and protect identities, HEINEKEN uses <select id="q4" onchange="checkAnswer('q4', 'DEFENDER FOR IDENTITY')"class="styled-dropdown">
    <option value="">Select an answer</option>
    <option value="DEFENDER FOR CLOUD">Defender for Cloud</option>
    <option value="DEFENDER FOR CLOUD APPS">Defender for Cloud Apps</option>
    <option value="DEFENDER FOR ENDPOINT">Defender for Endpoint</option>
    <option value="DEFENDER FOR IDENTITY">Defender for Identity</option>
   </select>.
   <span id="result4"></span>

<script>
  function checkAnswer(questionId, correctAnswer) {
    var selectedAnswer = document.getElementById(questionId).value;
    var resultId = 'result' + questionId.charAt(1);
    if (selectedAnswer === correctAnswer) {
      document.getElementById(resultId).innerText = 'Correct answer';
      document.getElementById(resultId).style.color = 'green';
    } else {
      document.getElementById(resultId).innerText = 'Try again';
      document.getElementById(resultId).style.color = 'red';
    }
  }
</script>
