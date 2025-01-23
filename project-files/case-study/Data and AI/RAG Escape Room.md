---
layout: default
title:  "RAG Escape Room"
category: "Case Study123"
sub-category: "Data and AI"
courses: [AI-102, AI-3016, AI-3018]
---

<html lang="en">
<head>

    <style>
        .room{
        justify-content: center;
        }

        .puzzle { 
            display: none; 
            background-color: #F1F1F1; 
            padding: 20px; 
            border-radius: 10px; 
            margin-bottom: 20px; 
        }
        .clue { 
            margin-top: 20px; 
            font-weight: bold; 
        }
        .puzzle input[type="radio"], .puzzle button { 
            margin: 10px auto; 
        }
        #intro {
            background-color: F1F1F1; 
            padding: 20px; 
            border-radius: 10px; 
        }
        .congratulations {
    color: blue;
    font-size: 24px;
    font-weight: bold;
      animation: blink-animation 1s steps(5, start) infinite;
    -webkit-animation: blink-animation 1s steps(5, start) infinite;
}

@keyframes blink-animation {
    to {
        visibility: hidden;
    }
}

@-webkit-keyframes blink-animation {
    to {
        visibility: hidden;
    }
}
    </style>
</head>
<body>
<div>
    <h1>Finding the Thief Misusing Azure AI Service Key</h1>
A company with three developers is facing an issue where someone is using the Azure AI service key for personal projects. Despite the admin's efforts to regenerate the key, the misuse continues. The company resources are new to Azure and are yet to learn about facilities like Azure Key Vault. 

<h2>Problem Statement </h2>
 The company needs to identify the person misusing the Azure AI service key. The admin has tried regenerating the key, but it hasn't been effective. The developers are new to Azure and are not familiar with facilities like Azure Key Vault that could help secure the keys. 

<h2>Developer Details </h2>

<ol>
      <li><strong>Alex</strong> Often leaves a coffee mug on their desk, often brings a laptop with a unique sticker, prefers to work in a quiet corner of the office, and often leaves the office just before lunch, usually visits the office early in the morning.</li>
      <li><strong>Jordan:</strong> Often leaves a coffee mug on their desk, usually visits the office early in the morning, often brings a laptop with a unique sticker, enjoys listening to classical music while working, and is known for their impeccable organizational skills, prefers to work in a quiet corner of the office. </li>
      <li><strong>Taylor</strong> Often leaves a coffee mug on their desk, often brings a laptop with a unique sticker, prefers to work in a quiet corner of the office, is an avid reader of mystery novels, and frequently participates in office trivia contests, usually visits the office early in the morning, </li>
           
</ol>

<h2>Objective</h2>
To solve the issue of key misuse, the company needs to identify the thief. The following MCQs will help in providing hints about the thief based on the correct answers. 
 
    <div class="room">
    <div id="intro">
        <h2>Welcome to the RAG Escape Room! Solve the puzzles and collect the hints to find the theif.</h2>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
    <div id="puzzle1" class="puzzle">
        <h2>Chapter 1: The Creative Campaign</h2>
        <h3>1.	What is the primary advantage of using RAG with Azure OpenAI over fine-tuning a model?</h3>
        <p>Which generative AI tool would be most suitable for generating creative content for your marketing campaign?</p>
        <label><input type="radio" name="answer1" value="a"> A) RAG requires less computational power</label><br>
        <label><input type="radio" name="answer1" value="b"> B) RAG eliminates the need for training a custom model with your data</label><br>
        <label><input type="radio" name="answer1" value="c"> C) RAG provides higher quality responses than fine-tuning</label><br>
        <label><input type="radio" name="answer1" value="d"> D) RAG allows for the use of larger datasets than fine-tuning</label><br>
        <button onclick="checkAnswer(1)">Submit</button>
        <button onclick="helpMe(1)">Help Me</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        <h2>Chapter 2: Customer Insights</h2>
        <h3>Next, you move to the customer feedback department. Your team needs to analyze customer feedback and generate summaries for quick insights.</h3>
        <p>Which Azure OpenAI model would you use to analyze customer feedback and generate summaries?</p>
        <label><input type="radio" name="answer2" value="a"> A) BERT</label><br>
        <label><input type="radio" name="answer2" value="b"> B) GPT</label><br>
        <label><input type="radio" name="answer2" value="c"> C) DALL-E</label><br>
        <label><input type="radio" name="answer2" value="d"> D) Azure Synapse Analytics</label><br>
        <button onclick="checkAnswer(2)">Submit</button>
        <button onclick="helpMe(2)">Help Me</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="puzzle3" class="puzzle">
        <h2>Chapter 3: The Chatbot Challenge</h2>
        <h3>Your journey continues to the customer support division, where you are tasked with creating a chatbot that can handle customer queries and provide personalized responses.</h3>
        <p>Which Azure service would you choose to implement a chatbot for handling customer queries?</p>
        <label><input type="radio" name="answer3" value="a"> A) Azure Bot Services</label><br>
        <label><input type="radio" name="answer3" value="b"> B) Azure Open AI services</label><br>
        <label><input type="radio" name="answer3" value="c"> C) AI Search</label><br>
        <label><input type="radio" name="answer3" value="d"> D) Azure Data Lake</label><br>
        <button onclick="checkAnswer(3)">Submit</button>
        <button onclick="helpMe(3)">Help Me</button>
        <div class="clue" id="clue3"></div>
    </div>
    <div id="puzzle4" class="puzzle">
        <h2>Chapter 4: System Messages</h2>
        <h3>In the next challenge, you need to ensure that the AI model provides responses that are aligned with the company's guidelines. You decide to use system messages to achieve this.</h3>
        <p>What is the purpose of using system messages in generative AI models?</p>
        <label><input type="radio" name="answer4" value="a"> A) To generate new content</label><br>
        <label><input type="radio" name="answer4" value="b"> B) To provide context and instructions to the AI model</label><br>
        <label><input type="radio" name="answer4" value="c"> C) To analyze data</label><br>
        <label><input type="radio" name="answer4" value="d"> D) To create images</label><br>
        <button onclick="checkAnswer(4)">Submit</button>
        <button onclick="helpMe(4)">Help Me</button>
        <div class="clue" id="clue4"></div>
    </div>
    <div id="puzzle5" class="puzzle">
        <h2>Chapter 5: Design Studio</h2>
        <h3>Your next stop is the design studio, where you need to create realistic images based on text descriptions for a design project.</h3>
        <p>Which generative AI model should you use to generate realistic images from text descriptions?</p>
        <label><input type="radio" name="answer5" value="a"> A) GPT</label><br>
        <label><input type="radio" name="answer5" value="b"> B) BERT</label><br>
        <label><input type="radio" name="answer5" value="c"> C) DALL-E</label><br>
        <label><input type="radio" name="answer5" value="d"> D) Azure Machine Learning</label><br>
        <button onclick="checkAnswer(5)">Submit</button>
        <button onclick="helpMe(5)">Help Me</button>
        <div class="clue" id="clue5"></div>
    </div>
    <div id="puzzle6" class="puzzle">
        <h2>Chapter 6: Data Analysis</h2>
        <h3>In the data analysis department, your team is tasked with generating detailed reports from large datasets.</h3>
        <p>Which Azure service would be best suited for generating detailed reports from large datasets?</p>
        <label><input type="radio" name="answer6" value="a"> A) Azure Data Factory</label><br>
        <label><input type="radio" name="answer6" value="b"> B) Azure Synapse Analytics</label><br>
        <label><input type="radio" name="answer6" value="c"> C) Azure Open AI services</label><br>
        <label><input type="radio" name="answer6" value="d"> D) Azure Cognitive Services</label><br>
        <button onclick="checkAnswer(6)">Submit</button>
        <button onclick="helpMe(6)">Help Me</button>
        <div class="clue" id="clue6"></div>
    </div>
    <div id="puzzle7" class="puzzle">
        <h2>Chapter 7: Temperature Control</h2>
        <h3>Your team is working on a creative writing project and needs to control the randomness of the AI-generated content. You decide to adjust the temperature parameter.</h3>
        <p>What effect does increasing the temperature parameter have on the AI-generated content?</p>
        <label><input type="radio" name="answer7" value="a"> A) It makes the content more deterministic</label><br>
        <label><input type="radio" name="answer7" value="b"> B) It increases the randomness and creativity of the content</label><br>
        <label><input type="radio" name="answer7" value="c"> C) It reduces the length of the content</label><br>
        <label><input type="radio" name="answer7" value="d"> D) It improves the accuracy of the content</label><br>
        <button onclick="checkAnswer(7)">Submit</button>
        <button onclick="helpMe(7)">Help Me</button>
        <div class="clue" id="clue7"></div>
    </div>
    <div id="puzzle8" class="puzzle">
        <h2>Chapter 8: Assistant APIs</h2>
        <h3>Finally, you need to maintain conversation context in your AI-powered application. You decide to use Assistant APIs for this purpose.</h3>
        <p>What is the primary benefit of using Assistant APIs in generative AI applications?</p>
        <label><input type="radio" name="answer8" value="a"> A) To generate images</label><br>
        <label><input type="radio" name="answer8" value="b"> B) To maintain conversation context</label><br>
        <label><input type="radio" name="answer8" value="c"> C) To analyze data</label><br>
        <label><input type="radio" name="answer8" value="d"> D) To create new models</label><br>
        <button onclick="checkAnswer(8)">Submit</button>
        <button onclick="helpMe(8)">Help Me</button>
        <div class="clue" id="clue8"></div>
    </div>
    <div id="finalChallenge" class="puzzle">
    <h2>Final Challenge: The Ultimate Test</h2>
    <h3>To complete your mission, you need to demonstrate your understanding of prompt engineering. Fill in the blank to complete the statement:</h3>
    <p>Effective prompt engineering involves crafting prompts that are clear, concise, and provide sufficient </p>
    <input type="text" id="finalAnswer" style="display: block; margin: 10px auto;"><br>
    <button onclick="checkFinalAnswer()">Submit</button>
    <button onclick="helpMe('final')">Help Me</button>
    <div class="clue" id="finalClue"></div>
    </div>
    </div>
<script>
    let currentPuzzle = 1;
    const clues = ["RAG eliminates the need for training a custom model with your data", "GPT", "Azure Bot Services", "To provide context and instructions to the AI model", "DALL-E", "Azure Synapse Analytics", "It increases the randomness and creativity of the content", "To maintain conversation context"];
    const correctAnswers = ["b", "b", "a", "b", "c", "b", "b", "b"];

    function startEscapeRoom() {
        document.getElementById('intro').style.display = 'none';
        showPuzzle(currentPuzzle);
    }

    function showPuzzle(puzzleNumber) {
        document.getElementById(`puzzle${puzzleNumber}`).style.display = 'block';
    }

    function checkAnswer(puzzleNumber) {
        const selectedOption = document.querySelector(`input[name="answer${puzzleNumber}"]:checked`);
        const clueElement = document.getElementById(`clue${puzzleNumber}`);

        if (selectedOption && selectedOption.value === correctAnswers[puzzleNumber - 1]) {
            clueElement.textContent = `Correct!`;
            clueElement.style.color = 'green';
            
            currentPuzzle++;
            if (currentPuzzle <= clues.length) {
                setTimeout(() => {
                    document.getElementById(`puzzle${puzzleNumber}`).style.display = 'none';
                    showPuzzle(currentPuzzle);
                }, 1000);
            } else {
                setTimeout(() => {
                    document.getElementById(`puzzle${puzzleNumber}`).style.display = 'none';
                    document.getElementById('finalChallenge').style.display = 'block';
                }, 1000);
            }
        } else {
            clueElement.textContent = 'Incorrect, try again!';
            clueElement.style.color = 'red';
        }
    }

    function helpMe(puzzleNumber) {
        if (puzzleNumber === 'final') {
            document.getElementById('finalAnswer').value = 'context';
        } else {
            document.querySelector(`input[name="answer${puzzleNumber}"][value="${correctAnswers[puzzleNumber - 1]}"]`).checked = true;
        }
    }

    function checkFinalAnswer() {
        const finalAnswer = document.getElementById('finalAnswer').value.toLowerCase();
        const finalClueElement = document.getElementById('finalClue');

        if (finalAnswer === 'context') {
            finalClueElement.textContent = 'CONGRATULATIONS! YOU HAVE ESCAPED THE ROOM !';
            finalClueElement.classList.add('congratulations');
        } else {
            finalClueElement.textContent = 'Incorrect, try again!';
            finalClueElement.style.color = 'red';
            finalClueElement.classList.remove('congratulations');
        }
    }
</script>
