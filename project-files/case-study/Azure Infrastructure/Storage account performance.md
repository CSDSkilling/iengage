---
layout: default
title:  "Storage Account Performance"
category: "Case Study"
sub-category: "Azure Infrastructure"
courses: [AZ-104, AZ-305, AZ-1003]
---
# Understanding Throttling in Azure Storage: A Fun Customer Support Scenario

## Introduction:

In the world of cloud storage, performance issues can sometimes slow down your operations, much like a traffic jam on a busy highway. One common culprit is throttling, which occurs when your storage account exceeds the allowed limits for Input/Output Operations Per Second (IOPS) or throughput. To help you understand this concept better, let's dive into a fun and engaging dialog between Evelyn, a customer, and Adam, a support representative. This scenario will illustrate how throttling works and what steps can be taken to resolve it. Enjoy the conversation and learn how to keep your Azure Storage running smoothly!


## Task 1: Listen to the conversation between Evelyn and Adam
<a href="./images/cc1.png">
  <img src="./images/cc1.png" alt="Evelyn talking to Adam over the phone" class="img-fluid">
</a>
<br>
<audio controls>
  <source src=" /iengage/project-files/case-study/Azure Infrastructure/videos/storageperformance.m4a" type="audio/mpeg"> 
  Your browser does not support the audio element.
</audio>


**Adam has decided to perform the following steps. What is Adam trying to achieve by performing the below steps? Click each option to find the reason**: 

   <button onclick="toggleSolution('solution1')">Monitor Metrics</button>
   <div id="solution1" style="display:none;">
     <p>The support representative will start by checking the Azure Monitor metrics for the storage account, focusing on IOPS and throughput usage. This helps identify if the limits are being exceeded.</p>
   </div>

  <button onclick="toggleSolution('solution2')">Analyze Usage Patterns</button>
   <div id="solution2" style="display:none;">
     <p>They will look at the usage patterns to understand when and why the limits are being hit. This includes checking for any spikes in activity or inefficient operations.</p>
   </div>

   <button onclick="toggleSolution('solution3')">Optimize Operations</button>
   <div id="solution3" style="display:none;">
     <p>The support representative will suggest optimizing the application's read/write operations. This could involve batching requests, reducing the frequency of operations, or optimizing the data access patterns.</p>
   </div>

   <button onclick="toggleSolution('solution4')">Upgrade Storage Tier</button>
   <div id="solution4" style="display:none;">
     <p>If the current storage tier is insufficient, the rep might recommend upgrading to a higher performance tier, such as Premium Storage, which offers higher IOPS and throughput limits.</p>
   </div>

   <button onclick="toggleSolution('solution5')">Implement Best Practices</button>
   <div id="solution5" style="display:none;">
     <p>They will ensure that best practices are being followed, such as using the appropriate storage tier for the workload, enabling caching where applicable, and optimizing network configurations.</p>
   </div>

  <button onclick="toggleSolution('solution6')">Monitor and Adjust</button>
   <div id="solution6" style="display:none;">
     <p>After making the necessary changes, the support representative will continue to monitor the performance to ensure the issue is resolved and make further adjustments if needed.</p>
   </div>


   <script>
     function toggleSolution(id) {
  var element = document.getElementById(id);
  if (element.style.display === "none") {
    element.style.display = "block";
  } else {
    element.style.display = "none";
  }
}
   </script>
