---
layout: default
title:  "Prompt Engineering"
category: "Gamification"
sub-category: "Data and AI"
courses: [AI-102, AI-3003]
---

# Prompt Engineering

## Introduction

Two colleagues Alex and Taylor are exploring the fascinating world of prompt engineering through a conversation. 
One of them is an expert in the field, while the other is a novice eager to learn. 
Through their interactions, the expert will teach the novice various techniques of prompt engineering. 
As they discuss and practice these techniques, the novice will gain a deeper understanding of how to craft effective prompts that can elicit accurate and useful responses from AI models. 

## The Basics of Prompt Engineering
This video showcases The Basics of Prompt Engineering.

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Data and AI/videos/PromptEngineering/PromptEng_player1.html?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

**Writing a clear, concise, and specific prompt:**
1.	Instead of just saying "Summarize this," you could say, "Please provide a concise summary of the main points in this document."
2.	Another example of Summarization- "Rewrite the introduction and conclusion of this document to be more concise while preserving the main point”
3.	While asking a question - "Explain how user authentication works in web applications for a beginner in web development”

**Providing clear context, and specifying the format of the output:**
1.	Providing Context: "As a 7th-grade science student, explain the process of photosynthesis in simple terms”
2.	Transcribe your meetings the right way: "Analyze this meeting transcript and summarize the meeting, especially all the key points made by a particular person.
3.	Specify the output format: "Provide a detailed summary of my recent emails about Copilot, output as a table with 4 columns: time, sender, description, did I respond to it”

## Common Mistakes to Avoid
This video showcases Common Mistakes to Avoid in Prompt Engineering.

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Data and AI/videos/PromptEngineering/PromptEng_player2.html?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

1. Being too vague: When a prompt is too vague, the LLM may provide a broad or irrelevant response. It's important to be specific to get the desired output.
Vague prompt: "Tell me about technology."
Specific prompt: "Explain the impact of artificial intelligence on healthcare."
Vague prompt: "Give me an image of a car."
Specific prompt: "Give me an image of a red Volvo XC90 from 2013."

2. Asking multiple questions in one prompt: Asking multiple questions in one prompt can confuse the LLM and result in incomplete or mixed responses. It's better to split them into separate prompts.
    Multiple questions: "What is LLM, and how does it work?"
    Separate prompts: "What is LLM?" and "How does LLM work?"
    Multiple questions: "Write a blog post about climate change and include recent statistics."
    Separate prompts: "List recent climate change statistics from 2023." and "Create an outline for a 	climate change blog post."


## Advance Prompt Engineering
This video showcases Advance Prompt Engineering.

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Data and AI/videos/PromptEngineering/PromptEng_player3.html?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

### 1. Prompt Chaining

Prompt chaining involves breaking down a complex task into a series of simpler, sequential prompts. Each prompt builds on the previous one to guide the model through a multi-step process.

#### Example: Task: Generate a detailed travel itinerary for a week-long trip to Japan.
Step 1: Generate a list of must-visit cities in Japan.
List the top 5 cities to visit in Japan for a week-long trip.
 
Step 2: For each city, list the top 3 tourist attractions.
For each of the following cities: Tokyo, Kyoto, Osaka, Hiroshima, and 	Nara, list the top 3 tourist attractions.
 
Step 3: Create a day-by-day itinerary incorporating the attractions.
Create a 7-day travel itinerary for Japan, including visits to the top 	attractions in Tokyo, Kyoto, Osaka, Hiroshima, and Nara.

### 2. Using Examples in a Prompt

Providing examples in a prompt helps the model understand the desired format and content of the response.
Example: Task: Generate a product description for an e-commerce website.
Prompt:
Write a product description for a new smartphone. Here are some examples 	of product descriptions:

	Example 1:
	Product: XYZ Smartphone
	Description: The XYZ Smartphone features a stunning 6.5-inch OLED display, 	 a powerful octa-core processor, and a long-lasting 4000mAh battery. With 	its advanced camera system, you can capture stunning photos and videos in 	any lighting condition. The sleek design and premium build quality make it 	 a perfect choice for tech enthusiasts.

	Example 2:
	Product: ABC Laptop
	Description: The ABC Laptop is designed for productivity and performance. 	It comes with a 15.6-inch Full HD display, an Intel i7 processor, and 16GB 	 of RAM. The 512GB SSD ensures fast boot times and ample storage for all 	your files. Whether you're working on a project or streaming your favorite 	 shows, the ABC Laptop delivers exceptional performance.

	Now, write a product description for a new smartphone.
