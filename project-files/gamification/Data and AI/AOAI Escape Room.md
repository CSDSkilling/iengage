---
layout: default
title:  "AOAI Escape Room"
category: "Gamification123"
sub-category: "Data and AI"
courses: [AI-102, AI-3016, AI-3018]
---

<html lang="en">
<head>

    <style>
        .room { 

            margin: 20px; 
            background-color: lightblue; 

        }

        .puzzle { 
            display: none; 
            background-color: lightgray; 
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
            background-color: lightblue; 
            padding: 20px; 
            border-radius: 10px; 
        }
    </style>
</head>
<body>
    <div class="room">
    <h1>Virtual AI Escape Room</h1>
    <div id="intro">
        <p>Welcome to the Virtual AI Escape Room! Solve the puzzles using your knowledge of Azure OpenAI to escape.</p>
        <button onclick="startEscapeRoom()">Start</button>
    </div>
    <div id="puzzle1" class="puzzle">
        <h2>Chapter 1: The Creative Campaign</h2>
        <h3>Your first task is to create a captivating marketing campaign for a new product launch. You need to generate creative content that will grab the audience's attention.</h3>
        <p>Which generative AI tool would be most suitable for generating creative content for your marketing campaign?</p>
        <label><input type="radio" name="answer1" value="a"> A) Azure Cognitive Services</label>
        <label><input type="radio" name="answer1" value="b"> B) Azure OpenAI services</label>
        <label><input type="radio" name="answer1" value="c"> C) Azure Machine Learning</label>
        <label><input type="radio" name="answer1" value="d"> D) Azure Data Factory</label>
        <button onclick="checkAnswer(1)">Submit</button>
        <button onclick="helpMe(1)">Help Me</button>
        <div class="clue" id="clue1"></div>
    </div>
    <div id="puzzle2" class="puzzle">
        <h2>Chapter 2: Customer Insights</h2>
        <h3>Next, you move to the customer feedback department. Your team needs to analyze customer feedback and generate summaries for quick insights.</h3>
        <p>Which Azure OpenAI model would you use to analyze customer feedback and generate summaries?</p>
        <label><input type="radio" name="answer2" value="a"> A) BERT</label>
        <label><input type="radio" name="answer2" value="b"> B) GPT</label>
        <label><input type="radio" name="answer2" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer2" value="d"> D) Azure Synapse Analytics</label>
        <button onclick="checkAnswer(2)">Submit</button>
        <button onclick="helpMe(2)">Help Me</button>
        <div class="clue" id="clue2"></div>
    </div>
    <div id="puzzle3" class="puzzle">
        <h2>Chapter 3: The Chatbot Challenge</h2>
        <h3>Your journey continues to the customer support division, where you are tasked with creating a chatbot that can handle customer queries and provide personalized responses.</h3>
        <p>Which Azure service would you choose to implement a chatbot for handling customer queries?</p>
        <label><input type="radio" name="answer3" value="a"> A) Azure Bot Services</label>
        <label><input type="radio" name="answer3" value="b"> B) Azure Open AI services</label>
        <label><input type="radio" name="answer3" value="c"> C) AI Search</label>
        <label><input type="radio" name="answer3" value="d"> D) Azure Data Lake</label>
        <button onclick="checkAnswer(3)">Submit</button>
        <button onclick="helpMe(3)">Help Me</button>
        <div class="clue" id="clue3"></div>
    </div>
    <div id="puzzle4" class="puzzle">
        <h2>Chapter 4: System Messages</h2>
        <h3>In the next challenge, you need to ensure that the AI model provides responses that are aligned with the company's guidelines. You decide to use system messages to achieve this.</h3>
        <p>What is the purpose of using system messages in generative AI models?</p>
        <label><input type="radio" name="answer4" value="a"> A) To generate new content</label>
        <label><input type="radio" name="answer4" value="b"> B) To provide context and instructions to the AI model</label>
        <label><input type="radio" name="answer4" value="c"> C) To analyze data</label>
        <label><input type="radio" name="answer4" value="d"> D) To create images</label>
        <button onclick="checkAnswer(4)">Submit</button>
        <button onclick="helpMe(4)">Help Me</button>
        <div class="clue" id="clue4"></div>
    </div>
    <div id="puzzle5" class="puzzle">
        <h2>Chapter 5: Design Studio</h2>
        <h3>Your next stop is the design studio, where you need to create realistic images based on text descriptions for a design project.</h3>
        <p>Which generative AI model should you use to generate realistic images from text descriptions?</p>
        <label><input type="radio" name="answer5" value="a"> A) GPT</label>
        <label><input type="radio" name="answer5" value="b"> B) BERT</label>
        <label><input type="radio" name="answer5" value="c"> C) DALL-E</label>
        <label><input type="radio" name="answer5" value="d"> D) Azure Machine Learning</label>
        <button onclick="checkAnswer(5)">Submit</button>
        <button onclick="helpMe(5)">Help Me</button>
        <div class="clue" id="clue5"></div>
    </div>
    <div id="puzzle6" class="puzzle">
        <h2>Chapter 6: Data Analysis</h2>
        <h3>In the data analysis department, your team is tasked with generating detailed reports from large datasets.</h3>
        <p>Which Azure service would be best suited for generating detailed reports from large datasets?</p>
        <label><input type="radio" name="answer6" value="a"> A) Azure Data Factory</label>
        <label><input type="radio" name="answer6" value="b"> B) Azure Synapse Analytics</label>
        <label><input type="radio" name="answer6" value="c"> C) Azure Open AI services</label>
        <label><input type="radio" name="answer6" value="d"> D) Azure Cognitive Services</label>
        <button onclick="checkAnswer(6)">Submit</button>
        <button onclick="helpMe(6)">Help Me</button>
        <div class="clue" id="clue6"></div>
    </div>
    <div id="puzzle7" class="puzzle">
        <h2>Chapter 7: Temperature Control</h2>
        <h3>Your team is working on a creative writing project and needs to control the randomness of the AI-generated content. You decide to adjust the temperature parameter.</h3>
        <p>What effect does increasing the temperature parameter have on the AI-generated content?</p>
        <label><input type="radio" name="answer7" value="a"> A) It makes the content more deterministic</label>
        <label><input type="radio" name="answer7" value="b"> B) It increases the randomness and creativity of the content</label>
        <label><input type="radio" name="answer7" value="c"> C) It reduces the length of the content</label>
        <label><input type="radio" name="answer7" value="d"> D) It improves the accuracy of the content</label>
        <button onclick="checkAnswer(7)">Submit</button>
        <button onclick="helpMe(7)">Help Me</button>
        <div class="clue" id="clue7"></div>
    </div>
    <div id="puzzle8" class="puzzle">
        <h2>Chapter 8: Assistant APIs</h2>
        <h3>Finally, you need to maintain conversation context in your AI-powered application. You decide to use Assistant APIs for this purpose.</h3>
        <p>What is the primary benefit of using Assistant APIs in generative AI applications?</p>
        <label><input type="radio" name="answer8" value="a"> A) To generate images</label>
        <label><input type="radio" name="answer8" value="b"> B) To maintain conversation context</label>
        <label><input type="radio" name="answer8" value="c"> C) To analyze data</label>
        <label><input type="radio" name="answer8" value="d"> D) To create new models</label>
        <button onclick="checkAnswer(8)">Submit</button>
        <button onclick="helpMe(8)">Help Me</button>
        <div class="clue" id="clue8"></div>
    </div>
    <div id="finalChallenge" class="puzzle">
    <h2>Final Challenge: The Ultimate Test</h2>
    <h3>To complete your mission, you need to demonstrate your understanding of prompt engineering. Fill in the blank to complete the statement:</h3>
    <p>Effective prompt engineering involves crafting prompts that are clear, concise, and provide sufficient </p>
    <input type="text" id="finalAnswer" style="display: block; margin: 10px auto;">
    <button onclick="checkFinalAnswer()">Submit</button>
    <button onclick="helpMe('final')">Help Me</button>
    <div class="clue" id="finalClue"></div>
    </div>
    </div>
<script>
    let currentPuzzle = 1;
    const clues = ["Azure OpenAI services", "GPT", "Azure Bot Services", "To provide context and instructions to the AI model", "DALL-E", "Azure Synapse Analytics", "It increases the randomness and creativity of the content", "To maintain conversation context"];
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
            clueElement.textContent = `Correct! Clue: ${clues[puzzleNumber - 1]}`;
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
            finalClueElement.textContent = 'Congratulations! You have escaped the room!';
        } else {
            finalClueElement.textContent = 'Incorrect, try again!';
        }
    }
</script>
</body>
</html>
