---
layout: default
title:  "Entra Verified ID in Municpal"
category: "Comic"
sub-category: "Security, Compliance and Identity"
courses: [SC-300, SC-5008]
---

# Microsoft Entra Verified ID in Municpal Services

## Introduction
In this dialog, a developer and an architect discuss the innovative ID wallet feature developed by Contoso, Inc. using Microsoft Entra Verified ID. They explore how this solution addresses the challenges faced by municipalities in managing paper certificates and administrative services. The conversation highlights the benefits of digitizing and centrally managing various certificates, the role of cloud services in reducing operational efforts, and the positive impact on both residents and local government efficiency. Through this discussion, the transformative potential of digital ID management in enhancing public services is clearly demonstrated.

<a href="./images/vid1.jpg" download>
  <img src="./images/vid1.jpg" alt="A four-panel comic strip featuring two business professionals discussing the ID wallet feature developed by Contoso. They talk about how the ID wallet digitizes and manages various credentials, integrates with Microsoft Entra Verified ID for secure digital ID management, allows residents to use the Contoso app for government services, and benefits local governments by streamlining administrative tasks and improving efficiency." class="img-fluid">
</a>

<a href="./images/vid2.jpg" download>
  <img src="./images/vid2.jpg" alt="A two-panel comic strip featuring a conversation between two business professionals. In the first panel, they discuss how Microsoft Entra Verified ID contributed to Contoso's development by providing a managed verifiable credential service, allowing Contoso to focus on the app's UI/UX while handling digital ID management through the cloud. In the second panel, they highlight how this partnership with Microsoft supported local governments in their digital transformation efforts, making administrative services more accessible and efficient for residents." class="img-fluid">
</a>

## Knowledge Check

Why is multi-factor authentication (MFA) considered essential for protecting sensitive project documents and client information?

<form id="quizForm">
  <input type="radio" id="q1" name="answer" value="q1">
  <label for="a1">  It makes logging in faster and more convenient.</label><br>
  <input type="radio" id="q2" name="answer" value="q2">
  <label for="a2">It blocks up to 99.9% of account compromise attacks, adding an extra layer of security.</label><br>
  <input type="radio" id="q3" name="answer" value="q3">
  <label for="a3">It eliminates the need for passwords entirely.</label><br>
  <input type="radio" id="q4" name="answer" value="q4">
  <label for="a4"> It only works for certain types of accounts.</label><br>
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
