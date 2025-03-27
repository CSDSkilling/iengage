---
layout: default
title:  "Azure Front Door Superhero"
category: "Gamification"
sub-category: "Azure Infrastructure"
courses: [AZ-305,AZ-700]
---
# Azure Front Door Superhero
In this interactive journey, you'll join our superhero, Azure Front Door, on a mission to ensure fast, reliable, and secure web content delivery. Each scene presents a unique challenge where you'll learn about the powerful features of Azure Front Door through fun and engaging activities.

## Scene 1: Introduction to Azure Front Door

**Meet Azure Front Door, your superhero for fast, reliable, and secure web content delivery!**
<br><br>
<a href="./images/fd1.png" download>
  <img src="./images/fd1.png" alt="Superhero posing and standing" class="img-fluid">
</a>

### What is Azure Front Door?
In the bustling city of Webville, a new hero has emerged. Azure Front Door, with its lightning-fast speed and impenetrable defenses, is here to ensure that web content reaches users swiftly and securely. As our story begins, Azure Front Door is ready to showcase its incredible abilities.

**Quiz Time!** Azure Front Door is eager to demonstrate its powers. Can you identify what it does best?
<br>
<select id="quiz-dropdown-1" onchange="checkAnswer1()" class="styled-dropdown">
  <option value="">Select an answer</option>
  <option value="correct">A) A global load balancer and CDN</option>
  <option value="wrong1">B) A database service</option>
  <option value="wrong2">C) A storage solution</option>
</select>
<p id="feedback-1"></p>

<script>
  function checkAnswer1() {
    var dropdown = document.getElementById("quiz-dropdown-1");
    var feedback = document.getElementById("feedback-1");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Think about what a superhero for web content delivery would do.";
      feedback.style.color = "red";
    }
  }
</script>


## Scene 2: The Quest for Optimization

**Our hero, Azure Front Door, embarks on a quest to optimize web content delivery!**
<br><br>
<a href="./images/fd2.jpeg" download>
  <img src="./images/fd2.jpeg" alt="Superhero flying and there is a text global delivery" class="img-fluid">
</a>

### Arrange the steps to set up Azure Front Door in the correct order:
Azure Front Door's journey to optimize your web content involves several key steps. Imagine our hero setting up a high-tech defense system to protect Webville. Each step is crucial for ensuring the city's safety and efficiency.

**Drag and Drop Challenge!**
<ul id="sortable-setup" class="styled-list">
  <li class="ui-state-default" data-order="1">Create a Front Door profile</li>
  <li class="ui-state-default" data-order="2">Add backend pools</li>
  <li class="ui-state-default" data-order="3">Configure routing rules</li>
  <li class="ui-state-default" data-order="4">Set up health probes</li>
</ul>

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>

<p id="feedback-setup"></p>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

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
      feedback.textContent = "Think about the logical sequence of setting up a defense system.";
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

## Scene 3: The Battle of Routing

**Azure Front Door uses intelligent routing to manage traffic and ensure optimal performance.**
<br><br>
<a href="./images/fd3.png" download>
  <img src="./images/fd3.png" alt="Superhero is monitoring the traffic" class="img-fluid">
</a>

### Select the correct routing method used by Azure Front Door:
Azure Front Door employs various routing methods to ensure users get the best experience. Picture our hero navigating through the busy streets of Webville, choosing the quickest and safest routes to deliver content.

**Quiz Time!**
<select id="quiz-dropdown-2" onchange="checkAnswer2()" class="styled-dropdown">
  <option value="">Select an answer</option>
  <option value="correct">A) Path-based routing</option>
  <option value="wrong1">B) IP-based routing</option>
  <option value="wrong2">C) DNS-based routing</option>
</select>
<p id="feedback-2"></p>

<script>
  function checkAnswer2() {
    var dropdown = document.getElementById("quiz-dropdown-2");
    var feedback = document.getElementById("feedback-2");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Think about the best path a superhero would take to navigate a city.";
      feedback.style.color = "red";
    }
  }
</script>

## Scene 4: The Final Challenge

**Azure Front Door faces its final challenge: ensuring security and reliability.**
<br><br>
<a href="./images/fd1.png" download>
  <img src="./images/fd1.png" alt="Superhero posing and standing to face the challenge" class="img-fluid">
</a>

### The Ultimate Defense
As Azure Front Door patrols the digital city of Webville, it encounters a series of cyber threats aiming to breach the city's defenses. But fear not! Azure Front Door is equipped with a powerful Web Application Firewall (WAF), a shield that deflects malicious attacks and keeps the city's data safe. This WAF is like an impenetrable barrier, blocking harmful traffic and ensuring that only legitimate users can access the city's resources.
<br>
Imagine a superhero's shield that not only blocks physical attacks but also neutralizes digital threats. With this shield, Azure Front Door can protect Webville from SQL injections, cross-site scripting, and other common vulnerabilities, ensuring the city's web applications remain secure and reliable.

**Quiz Time!** Azure Front Door is ready to deploy its ultimate defense. Which feature provides this robust protection?
<br>
<select id="quiz-dropdown-3" onchange="checkAnswer3()" class="styled-dropdown">
  <option value="">Select an answer</option>
  <option value="correct">A) Web Application Firewall (WAF)</option>
  <option value="wrong1">B) Database encryption</option>
  <option value="wrong2">C) Network isolation</option>
</select>
<p id="feedback-3"></p>

<script>
  function checkAnswer3() {
    var dropdown = document.getElementById("quiz-dropdown-3");
    var feedback = document.getElementById("feedback-3");
    if (dropdown.value === "correct") {
      feedback.textContent = "Correct!";
      feedback.style.color = "green";
    } else {
      feedback.textContent = "Think about a superhero's shield that protects against attacks.";
      feedback.style.color = "red";
    }
  }
</script>


