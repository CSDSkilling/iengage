---
layout: default
title:  "The Enchanted Vision Quest"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, PR-801, AI-3004]
---
# The Enchanted Vision Quest: Challenges Faced by Dr. Visionary

## Introduction

Dr. Visionary was on a magical mission to create an enchanted image classifier. His goal? To identify rare and magical creatures in the enchanted forest. Why, you ask? Well, rumour had it that these mystical beings held the secrets to eternal wisdom and boundless energy. Dr. Visionary believed that by cataloging these creatures, he could unlock their secrets and bring a new era of enlightenment and power to Techville. Plus, who wouldn't want to have a magical creature as a friend?

## The Magical Challenges
<br>
<a href="./images/m1.png" download>
  <img src="./images/m1.png" alt="picture of wizaed">
</a>

Just as Dr. Visionary thought he was nearing the end of his quest; he encountered an unexpected magical challenge. The problem is that Dr. Visionary's magic wand is broken, and it will take some time to fix it. He consulted the Head Wizard, who suggested using Custom Vision. Since Dr. Visionary has no idea about Custom Vision, can you help him match the problem statement with the appropriate solution?

**Match the Following:**

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sortable Setup</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
  <link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
  <style>
        .container {
      display: flex;
    }
    .column {
      flex: 1;
      padding: 10px;
    }
    .box {
      border: 1px solid #ccc;
      padding: 10px;
      margin: 5px 0;
      width: 300px;
      color: #007bff;
    }
    .styled-list {
      list-style-type: none;
      padding: 0;
    }
    .styled-list li {
      margin: 5px 0;
      padding: 10px;
      border: 1px solid #ccc;
      cursor: move;
    }

  </style>
</head>
<body>
  <div class="container">
    <div class="column">
      <div class="box">Create Custom Vision resources </div>
      <div class="box">Set up a new project </div>
      <div class="box">Collect training images </div>
      <div class="box">Upload and tag images </div>
      <div class="box">Train the classifier </div>
      <div class="box">Evaluate the classifier </div>
      <div class="box">Manage iterations</div>
    </div>
    <div class="column">
      <ul id="sortable-setup" class="styled-list">
        <li class="ui-state-default" data-order="3">Ensuring images meet specific criteria such as format and size</li>
        <li class="ui-state-default" data-order="2">Using the Custom Vision web page to start a new project</li>
        <li class="ui-state-default" data-order="1">Creating training and prediction resources in Azure</li>
        <li class="ui-state-default" data-order="4">Uploading images and assigning tags to them</li>
        <li class="ui-state-default" data-order="6">Evaluating the model performance with like precision and recall</li>
        <li class="ui-state-default" data-order="5">Using the collected images to create a model</li>
        <li class="ui-state-default" data-order="7">Managing multiple versions of the model to improve accuracy</li>
      </ul>
    </div>      
  </div>
<button onclick="checkOrderSetup()">Check Order</button>
      <button onclick="helpMeSetup()">Help me</button>
      <p id="feedback-setup"></p>
    
  <script>
    $(function() {
      $("#sortable-setup").sortable();
      $("#sortable-setup").disableSelection();
    });

    function checkOrderSetup() {
      var items = $("#sortable-setup li");
      var correct = true;
      items.each(function(index) {
        if ($(this).data("order") !== index + 1) {
          correct = false;
        }
      });
      var feedback = document.getElementById("feedback-setup");
      if (correct) {
        feedback.textContent = "Correct order!";
        feedback.style.color = "green";
      } else {
        feedback.textContent = "Incorrect order. Try again.";
        feedback.style.color = "red";
      }
    }

    function helpMeSetup() {
      var items = $("#sortable-setup li").sort(function(a, b) {
        return $(a).data("order") - $(b).data("order");
      });
      $("#sortable-setup").html(items);
      document.getElementById("feedback-setup").textContent = "Here is the correct order.";
      document.getElementById("feedback-setup").style.color = "blue";
    }
  </script>
</body>
</html>
