---
layout: default
title:  " AI Services for Retail"
category: "Case Study123"
sub-category: "Data and AI"
courses: [AI-102, PR-801]
---

<div class="fixed-buttons">

  <a href="#business" class="button">Business Overview</a>
  <a href="#existing" class="button">Existing Setup</a>
  <a href="#new" class="button">New Requirement</a>
</div>


<br><br>


# Case Study: Transforming Retail Operations with Azure AI Services

## Business Overview
<a id="business"></a>
Lakeshore Retail, a prominent retail chain with over 500 stores nationwide, offers a diverse range of products from groceries to electronics and maintains a strong online presence. Lakeshore Retail goals include enhancing customer experience, streamlining operations, and leveraging data for informed decision-making.

## Existing Setup
<a id="existing"></a>
Lakeshore Retail's robust IT infrastructure includes:
1. **Point of Sale (POS) Systems:** Integrated with inventory management.
2. **Customer Relationship Management (CRM):** For managing customer data and interactions.
3. **E-commerce Platform:** Supporting online sales and customer engagement.
4. **Data Warehousing:** For storing and analyzing sales and customer data.

## New Requirement
<a id="new"></a>
Lakeshore Retail has identified several areas for improvement:
1. **Enhanced Customer Experience:** Personalizing customer interactions both online and in-store.
   - Virtual Try-On Feature: Lakeshore Retail is planning to launch the virtual 'Try-It-On' feature with their range of eyewear products such as sunglasses, swimming goggles, and spectacles. Customers will be able to upload a front-profile selfie and see how the eyewear fits.
   - In-Store Touch Screen Assistant: Enhancing the touch-screen assistant in retail outlets with mic input and read-aloud functionality.
   - Digital Assistant: Creating a digital assistant for their e-commerce platform to assist customers with order details, return policies, etc.
   - Sentiment Analysis: Analyzing product reviews to recommend more suitable products to customers.
   - Image-Based Search: Add an option in the E-commerce site, where customers can upload an image and search for similar items in the inventory.
2. **Streamline Business Operations**
    - Customer Purchase Analysis: Analyzing customer purchase invoices to identify patterns and draw business conclusions.
    - Social Media Analysis: Analyzing tweets to identify key topics being discussed about Lakeshore Retail.
3. **Business Expansion and Compliance**
    - Age Verification: Lakeshore Retail plans to expand its business by adding a liquor section in their retail outlets. To ensure minors cannot order liquor through the Touch-Screen Assistants, it will implement age verification for customers purchasing alcohol.

 

**Question 1:** Which Azure AI service can they use to implement the virtual Try-It-On feature, to identify the position of the eyes in an uploaded image ?
<form id="quizForm1">
  <input type="radio" id="q1a" name="q1" value="A">
  <label for="q1a">A) Azure Cognitive Service </label><br>
  <input type="radio" id="q1b" name="q1" value="B">
  <label for="q1b">B) Azure Bot Service</label><br>
  <input type="radio" id="q1c" name="q1" value="C">
  <label for="q1c">C) Face API </label><br>
  <input type="radio" id="q1d" name="q1" value="D">
  <label for="q1d">D) Azure Computer Vision </label><br>
  <button type="button" onclick="checkAnswer('q1', 'C', 'result1')" class="styled-button">Submit</button>
</form>
<p id="result1"></p>

**Question 2:** Lakeshore Retail wants to use the Azure AI Language Service to analyze product reviews and suggest products with higher positive reviews to customers. Which class and method should be used to analyze the product reviews using the Azure AI Language Service SDK in C#?
<form id="quizForm2">
  <input type="radio" id="q2a" name="q2" value="A">
  <label for="q2a">A) TextAnalyticsClient class and AnalyzeSentiment method </label><br>
  <input type="radio" id="q2b" name="q2" value="B">
  <label for="q2b">B) TextAnalyticsClient class and ExtractKeyPhrases method</label><br>
  <input type="radio" id="q2c" name="q2" value="C">
  <label for="q2c">C) LanguageClient class and ExtractKeyPhrases method</label><br>
  <input type="radio" id="q2d" name="q2" value="D">
  <label for="q2d">D) LanguageClient class and AnalyzeSentiment method </label><br>

  <button type="button" onclick="checkAnswer('q2', 'A', 'result2')" class="styled-button">Submit</button>
</form>

<p id="result2"></p>

**Question 3:** Which AI service and feature should the developers implement a read-aloud feature for visually impaired users in their Touch Screen Assistant at retail outlets?

<form id="quizForm3">
  <input type="radio" id="q3a" name="q3" value="A">
  <label for="q3a">A) Azure AI Vision Service with Optical Character Recognition (OCR) </label><br>
  <input type="radio" id="q3b" name="q3" value="B">
  <label for="q3b">B) Azure AI Language Service with Text Analytics</label><br>
  <input type="radio" id="q3c" name="q3" value="C">
  <label for="q3c">C) Azure AI Speech Service with Text-to-Speech (TTS) </label><br>
  <input type="radio" id="q3d" name="q3" value="D">
  <label for="q3d">D) Azure AI Bot Service with QnA Maker </label><br>
  <button type="button" onclick="checkAnswer('q3', 'C', 'result3')" class="styled-button">Submit</button>
</form>

<p id="result3"></p>

**Question 4:** Lakeshore Retail wants to analyze tweets about the company to identify key discussion topics. Which endpoint will you use for social media analysis?

**Question 5:** How can Lakeshore Retail implement the new requirement for image-based search?

<div class="column">
  <ul id="sortable-setup" class="styled-list">
    <li class="ui-state-default" data-order="4">Define the custom skill in the skillset.</li>
    <li class="ui-state-default" data-order="6">Test the search functionality.</li>
    <li class="ui-state-default" data-order="5">Add the custom skill to the indexer.</li>
    <li class="ui-state-default" data-order="2">Configure the data source.</li>
    <li class="ui-state-default" data-order="3">Deploy the custom skill to an Azure Function.</li>
    <li class="ui-state-default" data-order="1">Create an Azure AI Search service.</li>
  </ul>
</div>  

<button onclick="checkOrderSetup()">Check Order</button>
<button onclick="helpMeSetup()">Help me</button>
<p id="feedback-setup"></p>


**Question 6:**

<div class="container">
  <!-- Left Column -->
  <div class="column" id="left-column">
    <div class="draggable-item" draggable="true" id="item1">Require the buyer to upload a valid government photo-ID card</div>
    <div class="draggable-item" draggable="true" id="item2">Use a barcode scanner to scan the ID</div>
    <div class="draggable-item" draggable="true" id="item3">Implement a manual verification process by store staff</div>
    <div class="draggable-item" draggable="true" id="item4">Take a picture of the buyer at the time of purchase</div>
    <div class="draggable-item" draggable="true" id="item5">Verify the buyer's age through their social media profiles.</div>
    <div class="draggable-item" draggable="true" id="item6">Extract information such as expiry date and date of birth from the ID using Azure AI Document Intelligence.</div>
    <div class="draggable-item" draggable="true" id="item7">Match the photo on the ID with the buyer's photo using the face comparison feature in Azure Face API service.</div>
    <div class="draggable-item" draggable="true" id="item8">Match the photo on the ID with the buyer's photo using the attribute analysis feature in Azure AI Vision service.</div>
    <div class="draggable-item" draggable="true" id="item9">Implement a voice recognition system to verify the buyer's age.</div>    
  </div>

  <!-- Right Column -->
  <div class="column" id="right-column">
    <div class="placeholder" id="placeholder1" data-accept="item1></div>
    <div class="placeholder" id="placeholder2" data-accept="item6"></div>
    <div class="placeholder" id="placeholder3" data-accept="item7"></div>
  </div>
</div>

  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.min.js"></script>
  <link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<script>
  function checkAnswer(question, correctAnswer, resultId) {
    var radios = document.getElementsByName(question);
    var result = document.getElementById(resultId);
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

     // Add drag-and-drop functionality
  const draggableItems = document.querySelectorAll('.draggable-item');
  const placeholders = document.querySelectorAll('.placeholder');

  draggableItems.forEach((item) => {
    item.addEventListener('dragstart', (e) => {
      e.dataTransfer.setData('text/plain', e.target.id);
      setTimeout(() => {
        item.style.display = 'none';
      }, 0);
    });

    item.addEventListener('dragend', (e) => {
      item.style.display = 'block';
    });
  });

  placeholders.forEach((placeholder) => {
    placeholder.addEventListener('dragover', (e) => {
      e.preventDefault();
      placeholder.classList.add('over');
    });

    placeholder.addEventListener('dragleave', (e) => {
      placeholder.classList.remove('over');
    });

    placeholder.addEventListener('drop', (e) => {
      e.preventDefault();
      const itemId = e.dataTransfer.getData('text/plain');
      const draggedItem = document.getElementById(itemId);

       if (placeholder.dataset.accept === itemId) {
        placeholder.appendChild(draggedItem);
        placeholder.classList.remove('over');
        placeholder.textContent = `Item Placed: ${draggedItem.textContent}`;
      } else {
        alert(`This placeholder only accepts ${placeholder.dataset.accept}.`);
        placeholder.classList.remove('over');
      }
      
      
    });
  });
  
</script>

<style>
.fixed-buttons {
  position: fixed;
  top: 0;
  width: 100%;
  background-color: white; /* Optional: to match the background */
  display: flex;
  padding: 10px 0;
  z-index: 1000; /* Ensure it stays on top of other content */
}

.button {
  margin: 0 10px;
  padding: 10px 20px;
  background-color: #0078d4;
  color: white;
  text-decoration: none;
  border-radius: 5px;
}

.button:hover {
  background-color: #0056b3;
}

    .column {
      flex: 1;
      padding: 10px;
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

    .container {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }

  .column {
    flex: 1;
    margin: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    min-height: 300px;
  }

  .draggable-item {
    margin: 20px 0;
    padding: 10px;
    border: 1px solid #0078d4;
    background-color: #e7f3ff;
    cursor: grab;
  }

  .placeholder {
    margin: 10px 0;
    padding: 20px;
    border: 2px dashed #ccc;
    background-color: #f9f9f9;
    text-align: center;
    min-height: 50px;
  }

  .placeholder.over {
    border-color: #0078d4;
    background-color: #d4e8ff;
  }

</style>
