---
layout: default
title:  "Document Intelligence for Handwritten"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3002]
---

# Transforming Manuscript Management with Document Intelligence

## Introduction
In a library filled with countless handwritten manuscripts, managing and searching through these valuable documents can be a daunting task. However, document intelligence offers a revolutionary solution. This dialogue between Alice, Bob, Charlie, and David explores how AI-powered document intelligence can digitize, organize, and preserve handwritten manuscripts, making them easily searchable and accessible. The conversation highlights the potential of this technology to transform the way we handle historical documents, opening up new possibilities for research and preservation.
<a href="./images/di1.png" download>
  <img src="./images/di1.png" alt="A group of four people in a library analying old manuscripts">
</a>
### Question 1
**Charlie says "....convert handwritten text into digital text, recognizing different handwriting styles and extracting key information.". How is this done in document intelligence?**

<form id="question1Form">
    <label><input type="radio" name="question1" value="A"> A) By manually typing out the handwritten text.</label><br>
    <label><input type="radio" name="question1" value="B"> B) By using Optical Character Recognition (OCR) and machine learning to scan and convert handwritten text into digital text.</label><br>
    <label><input type="radio" name="question1" value="C"> C) By photographing the documents and storing the images as they are.</label><br>
    <label><input type="radio" name="question1" value="D"> D) By using prebuilt models to analyze and categorize the documents without converting the text.</label><br>
    <button type="button" onclick="checkAnswer1()">Submit</button>
</form>
<div id="result1"></div>

### Question 2
**Do you agree with David's statement ".. it can categorize and organize the documents, identify duplicates, and flag important sections."? If yes, which of the below points is true?**

<form id="question2Form">
    <label><input type="checkbox" name="question2" value="A"> A) Document intelligence uses Optical Character Recognition (OCR) to convert handwritten text into digital text.</label><br>
    <label><input type="checkbox" name="question2" value="B"> B) Document intelligence uses machine learning to categorize and organize documents based on their content and context.</label><br>
    <label><input type="checkbox" name="question2" value="C"> C) Document intelligence can identify duplicates by comparing document content and metadata.</label><br>
    <label><input type="checkbox" name="question2" value="D"> D) Document intelligence can flag important sections by analyzing document structure and extracting key information.</label><br>
    <button type="button" onclick="checkAnswer2()">Submit</button>
</form>
<div id="result2"></div>



**Alice, Bob, Charlie and David share their findings with development team.**

<a href="./images/di2.png" download>
  <img src="./images/di2.png" alt="2 developers discussing">
</a>

### Question 3
**How do you create a custom model in document intelligence?**

<form id="question3Form">
    <label><input type="radio" name="question3" value="A"> A) By manually labeling each document without any automation.</label><br>
    <label><input type="radio" name="question3" value="B"> B) By using prebuilt models without any customization.</label><br>
    <label><input type="radio" name="question3" value="C"> C) By uploading training data, labeling the data, and training the model using Azure AI Document Intelligence.</label><br>
    <label><input type="radio" name="question3" value="D"> D) By using only text-based documents without any images.</label><br>
    <button type="button" onclick="checkAnswer3()">Submit</button>
</form>
<div id="result3"></div>

### Question 4
**How can developers ensure the accuracy and reliability of a custom document intelligence model?**

<form id="question4Form">
    <label><input type="checkbox" name="question4" value="A"> A) By continuously updating the training data with new examples.</label><br>
    <label><input type="checkbox" name="question4" value="B"> B) By using only prebuilt models without customization.</label><br>
    <label><input type="checkbox" name="question4" value="C"> C) By performing extensive testing and validation.</label><br>
    <label><input type="checkbox" name="question4" value="D"> D) By ignoring user feedback and focusing solely on initial training data.</label><br>
    <button type="button" onclick="checkAnswer4()">Submit</button>
</form>
<div id="result4"></div>

<script>
    function checkAnswer1() {
        const correctAnswer = 'B';
        const form = document.getElementById('question1Form');
        const selected = form.querySelector('input[name="question1"]:checked');
        const result = document.getElementById('result1');
        result.innerHTML = '';
        if (selected) {
            if (selected.value === correctAnswer) {
                result.innerHTML = '<p style="color: green;">Correct! By using Optical Character Recognition (OCR) and machine learning to scan and convert handwritten text into digital text.</p>';
            } else {
                result.innerHTML = '<p style="color: red;">Incorrect. The correct answer is B.</p>';
            }
        } else {
            result.innerHTML = '<p style="color: red;">Please select an answer.</p>';
        }
    }

    function checkAnswer2() {
        const correctAnswers = ['B', 'C', 'D'];
        const form = document.getElementById('question2Form');
        const selected = Array.from(form.querySelectorAll('input[name="question2"]:checked')).map(input => input.value);
        const result = document.getElementById('result2');
        result.innerHTML = '';
        let allCorrect = true;
        correctAnswers.forEach(answer => {
            const label = form.querySelector(`input[value="${answer}"]`).parentElement;
            if (selected.includes(answer)) {
                label.style.color = 'green';
            } else {
                label.style.color = 'red';
                allCorrect = false;
            }
        });
        selected.forEach(answer => {
            if (!correctAnswers.includes(answer)) {
                const label = form.querySelector(`input[value="${answer}"]`).parentElement;
                label.style.color = 'red';
                allCorrect = false;
            }
        });
        if (allCorrect) {
            result.innerHTML = '<p style="color: green;">Correct! Document intelligence uses machine learning to categorize and organize documents based on their content and context, Document intelligence can identify duplicates by comparing document content and metadata, Document intelligence can flag important sections by analyzing document structure and extracting key information </p>';
        } else {
            result.innerHTML = '<p style="color: red;">Some answers are incorrect. The correct answers are B, C, and D.</p>';
        }
    }

     function checkAnswer3() {
        const correctAnswer = 'C';
        const form = document.getElementById('question3Form');
        const selected = form.querySelector('input[name="question3"]:checked');
        const result = document.getElementById('result3');
        result.innerHTML = '';
        if (selected) {
            if (selected.value === correctAnswer) {
                result.innerHTML = '<p style="color: green;">Correct! By uploading training data, labeling the data, and training the model using Azure AI Document Intelligence.</p>';
            } else {
                result.innerHTML = '<p style="color: red;">Incorrect. The correct answer is C. By uploading training data, labeling the data, and training the model using Azure AI Document Intelligence.</p>';
            }
        } else {
            result.innerHTML = '<p style="color: red;">Please select an answer.</p>';
        }
    }

      function checkAnswer4() {
        const correctAnswers = ['A', 'C'];
        const form = document.getElementById('question4Form');
        const selected = Array.from(form.querySelectorAll('input[name="question4"]:checked')).map(input => input.value);
        const result = document.getElementById('result4');
        result.innerHTML = '';
        let allCorrect = true;
        correctAnswers.forEach(answer => {
            const label = form.querySelector(`input[value="${answer}"]`).parentElement;
            if (selected.includes(answer)) {
                label.style.color = 'green';
            } else {
                label.style.color = 'red';
                allCorrect = false;
            }
        });
        selected.forEach(answer => {
            if (!correctAnswers.includes(answer)) {
                const label = form.querySelector(`input[value="${answer}"]`).parentElement;
                label.style.color = 'red';
                allCorrect = false;
            }
        });
        if (allCorrect) {
            result.innerHTML = '<p style="color: green;">Correct! By continuously updating the training data with new examples and performing extensive testing and validation, developers can ensure the accuracy and reliability of a custom document intelligence model.</p>';
        } else {
            result.innerHTML = '<p style="color: red;">Some answers are incorrect. The correct answers are A and C.</p>';
        }
    }
  
</script>

