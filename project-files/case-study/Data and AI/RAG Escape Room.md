---
layout: default
title:  "RAG Escape Room"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, AI-3016, AI-3018, PR-801]
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

    <a href="./images/es1.png">
  <img src="./images/es1.png" alt="a group of people looking at computer">
</a>
    <div class="instructions">
        <h3>How to Play</h3>
        <ol>
            <li><strong>Start the Game:</strong> Click the <strong>"Start"</strong> button on the introduction screen to begin your escape room adventure.</li>
            <li><strong>Solve Puzzles:</strong> You will be presented with a series of puzzles, each related to Azure OpenAI concepts. Read the question carefully and select the correct answer by clicking on the corresponding radio button. Click the <strong>"Submit"</strong> button to check your answer.</li>
            <li><strong>Get Help:</strong> If you're stuck on a puzzle, you can click the <strong>"Help Me"</strong> button to reveal the correct answer. Use this option sparingly to challenge yourself!</li>
            <li><strong>Collect Clues:</strong> For each correct answer, you will receive a clue. Pay attention to these clues as they will help you in the final challenge.</li>
            <li><strong>Progress Through Puzzles:</strong> After submitting a correct answer, the next puzzle will automatically appear after 8 seconds. Continue solving puzzles until you reach the final challenge.</li>        
            <li><strong>Complete the Game:</strong> If your final answer is correct, you will see a congratulatory message indicating that you have escaped the room. If your answer is incorrect, you can try again or use the <strong>"Help Me"</strong> button for assistance.</li>
        </ol>
</div>

 
    <div class="room">
    <div id="intro">
        <h2>Welcome to the RAG Escape Room! Solve the puzzles and collect the hints to find the theif.</h2>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
    <div id="puzzle1" class="puzzle">
        
        <h3>1.	What is the primary advantage of using RAG with Azure OpenAI over fine-tuning a model?</h3>
        
        <label><input type="radio" name="answer1" value="a"> A) RAG requires less computational power</label><br>
        <label><input type="radio" name="answer1" value="b"> B) RAG eliminates the need for training a custom model with your data</label><br>
        <label><input type="radio" name="answer1" value="c"> C) RAG provides higher quality responses than fine-tuning</label><br>
        <label><input type="radio" name="answer1" value="d"> D) RAG allows for the use of larger datasets than fine-tuning</label><br>
        <button onclick="checkAnswer(1)">Submit</button>
        <button onclick="helpMe(1)">Help Me</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        
        <h3>2.	What is the role of Azure Search in RAG?</h3>
        
        <label><input type="radio" name="answer2" value="a"> A) It generates random data for the model</label><br>
        <label><input type="radio" name="answer2" value="b"> B) It provides context by generating indexes from various data sources</label><br>
        <label><input type="radio" name="answer2" value="c"> C) It replaces the need for prompts</label><br>
        <label><input type="radio" name="answer2" value="d"> D) It only works with SQL databases</label><br>
        <button onclick="checkAnswer(2)">Submit</button>
        <button onclick="helpMe(2)">Help Me</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="puzzle3" class="puzzle">
      
        <h3>3.	How Which of the following is a key benefit of fine-tuning a model compared to using RAG?</h3>
      
        <label><input type="radio" name="answer3" value="a"> A) Fine-tuning is less costly and time-intensive</label><br>
        <label><input type="radio" name="answer3" value="b"> B) Fine-tuning allows for customization on examples larger than can fit in a prompt</label><br>
        <label><input type="radio" name="answer3" value="c"> C) Fine-tuning eliminates the need for a stateless API</label><br>
        <label><input type="radio" name="answer3" value="d"> D) Fine-tuning provides immediate responses without the need for grounding data</label><br>
        <button onclick="checkAnswer(3)">Submit</button>
        <button onclick="helpMe(3)">Help Me</button>
        <div class="clue" id="clue3"></div>
    </div>

<div id="puzzle4" class="puzzle">
    <h3>4. Which of the following steps are involved in the RAG process with Azure OpenAI on your data? (Select all that apply)</h3>
    
    <label><input type="checkbox" name="answer4" value="a"> A) Receive user prompt</label><br>
    <label><input type="checkbox" name="answer4" value="b"> B) Train a custom model with your data</label><br>
    <label><input type="checkbox" name="answer4" value="c"> C) Determine relevant content</label><br>
    <label><input type="checkbox" name="answer4" value="d"> D) Query the search index</label><br>
    <label><input type="checkbox" name="answer4" value="e"> E) Insert search result into the Azure OpenAI prompt, along with user prompt</label><br>
    <label><input type="checkbox" name="answer4" value="f"> F) Return response and data reference (if any) to the user</label><br>
    <button onclick="checkAnswer(4)">Submit</button>
    <button onclick="helpMe(4)">Help Me</button>
    <div class="clue" id="clue4"></div>
</div>

     <div id="puzzle5" class="puzzle">
        <h2>Final Challenge: The Ultimate Test</h2>
  
        <p>Azure Open ai enables RAG by connecting ________ models to your own data source</p>
        <label><input type="radio" name="answer5" value="a"> A) Pre-trained models</label><br>
        <label><input type="radio" name="answer5" value="b"> B) Fine-tuned models</label><br>
        
        <button onclick="checkAnswer(5)">Submit</button>
        <button onclick="helpMe(5)">Help Me</button>
        <div class="clue" id="clue5"></div>
    </div>

</div>
<script>
 let currentPuzzle = 1;
const clues = ["The thief often leaves a coffee mug on their desk", "The thief usually visits the office early in the morning", "The thief often brings a laptop with a unique sticker.", "The thief prefers to work in a quiet corner of the office", "The thief often leaves the office just before lunch."];

const correctAnswers = {
    1: ["b"],
    2: ["b"],
    3: ["d"],
    4: ["a", "c", "d", "e", "f"],
    5: ["a"]
};


function startEscapeRoom() {
    document.getElementById('intro').style.display = 'none';
    showPuzzle(currentPuzzle);
}

function showPuzzle(puzzleNumber) {
    document.getElementById(`puzzle${puzzleNumber}`).style.display = 'block';
}

function checkAnswer(puzzleNumber) {
    const selectedOptions = document.querySelectorAll(`input[name="answer${puzzleNumber}"]:checked`);
    const clueElement = document.getElementById(`clue${puzzleNumber}`);
    const selectedValues = Array.from(selectedOptions).map(option => option.value);

    if (arraysEqual(selectedValues, correctAnswers[puzzleNumber])) {
        clueElement.textContent = `Correct! Clue: ${clues[puzzleNumber - 1]}`;
        clueElement.style.color = 'green';
        
        setTimeout(() => {
            document.getElementById(`puzzle${puzzleNumber}`).style.display = 'none';
            currentPuzzle++;
            if (currentPuzzle <= Object.keys(clues).length) {
                showPuzzle(currentPuzzle);
            } else {
                displayCongratulations();
            }
        }, 5000); // Stay on the current question for 5 seconds
    } else {
        clueElement.textContent = 'Incorrect, try again!';
        clueElement.style.color = 'red';
    }
}

function arraysEqual(arr1, arr2) {
    return arr1.length === arr2.length && arr1.every(value => arr2.includes(value));
}


function displayCongratulations() {

  const roomDiv = document.querySelector('.room');
    roomDiv.innerHTML = '<div class="congratulations">CONGRATULATIONS! YOU HAVE ESCAPED THE ROOM!</div>';
    
}

function helpMe(puzzleNumber) {   

   const correctOptions = correctAnswers[puzzleNumber];
    correctOptions.forEach(option => {
        document.querySelector(`input[name="answer${puzzleNumber}"][value="${option}"]`).checked = true;
    });
}

 
</script>
