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

<script>
    function checkAnswer1() {
        const correctAnswer = 'B';
        const form = document.getElementById('question1Form');
        const selected = form.querySelector('input[name="question1"]:checked');
        const result = document.getElementById('result1');
        result.innerHTML = '';
        if (selected) {
            if (selected.value === correctAnswer) {
                result.innerHTML = '<p style="color: green;">Correct!</p>';
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
            result.innerHTML = '<p style="color: green;">Correct!</p>';
        } else {
            result.innerHTML = '<p style="color: red;">Some answers are incorrect. The correct answers are B, C, and D.</p>';
        }
    }
</script>
Alice, Bob, Charlie and David share their findings with development team. 

<a href="./images/di2.png" download>
  <img src="./images/di2.png" alt="2 developers discussing">
</a>

