---
layout: default
title:  "Multilingual Customer Support"
category: "Case Study"
sub-category: "Data and AI"
courses: [AI-102, AI-3003, PR-801]
---

# Multilingual Customer Support

## Introduction:

This is a dialog between Hiroshi and Amanda. Amanda works for a call center that handles customer inquiries from around the world. To provide efficient and personalized support, they leverage AI services.<br>
**Situation:** A customer from Japan calls the support line to inquire about a recent order. The customer speaks only Japanese, while the available support agent speaks only English.

## Task 1: Listen to the conversation between Hiroshi and Amanda

<a href="./images/cc.png">
  <img src="./images/cc.png" alt="Amanda talking to Hiroshi over the phone">
</a>
<br>
<audio controls>
  <source src=" /iengage/project-files/gamification/Data and AI/videos/callcenter.m4a" type="audio/mpeg"> 
  Your browser does not support the audio element.
</audio>

**Question** Which AI service enabled Amanda to respond to Hiroshi, even though she didn't speak Japanese?


<div class="button-container">
    <button id="a1" onclick="markAnswer(this, false, 'result')">Detect Language</button>
    <button id="a2" onclick="markAnswer(this, true, 'result')">Speech Translation</button>
    <button id="a3" onclick="markAnswer(this, false, 'result')">Translate Service</button>
</div>
<p id="result"></p>

## Task 2: Observe the below image where Amanda is chatting with a Japanese customer <br>

<a href="./images/cc2.png">
  <img src="./images/cc2.png" alt="Amanda talking to Hiroshi over the chat">
</a>
<br>

**Question** Which service helps with the translation here?
<div class="button-container">
    <button id="a21" onclick="markAnswer(this, false, 'result1')">Detect Language</button>
    <button id="a22" onclick="markAnswer(this, false, 'result1')">Speech Translation</button>
    <button id="a23" onclick="markAnswer(this, true, 'result1')">Translate Service</button>
</div>
<p id="result1"></p>

## Task 3: Help the architects with the below questions

<a href="./images/arch.png">
  <img src="./images/arch.png" alt="a group of architects discussing">
</a>


 1. How do AI services like Speech-to-Text and Text-to-Speech improve the accuracy of customer interactions?
    <button onclick="toggleSolution('solution1')">Show Solution</button>
    <div id="solution1" style="display:none;">
        <div class="benefit">
            <p class="benefit-title">Enhanced Understanding:</p>
            <p>Speech-to-Text (STT) converts spoken language into written text with high accuracy, ensuring that customer queries are accurately captured.</p>
        </div>
        <div class="benefit">
            <p class="benefit-title">Clear Communication:</p>
            <p>Text-to-Speech (TTS) converts text responses into natural-sounding speech, making it easier for customers to understand the information provided.</p>
        </div>
        <div class="benefit">
            <p class="benefit-title">Real-Time Processing:</p>
            <p>Both STT and TTS operate in real-time, allowing for immediate transcription and response, which reduces misunderstandings and improves the flow of conversation.</p>
        </div>
    </div>

2. How can SSML be used to enhance the naturalness and expressiveness of Text-to-Speech (TTS) outputs in a call center environment?
    <button onclick="toggleSolution('solution2')">Show Solution</button>
    <div id="solution2" style="display:none;">
        <div class="benefit">
            <p class="benefit-title">Prosody Control:</p>
            <p>SSML allows you to adjust the pitch, rate, and volume of the synthesized speech. This can make the speech sound more natural and engaging. For example, increasing the pitch slightly for a greeting can make it sound more friendly.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;&lt;prosody pitch="+10%"&gt;Hello, how can I assist you today?&lt;/prosody&gt;<br>
                &lt;/speak&gt;
            </code>
        </div>
        <div class="benefit">
            <p class="benefit-title">Pauses and Breaks:</p>
            <p>You can insert pauses or breaks at appropriate places to mimic natural speech patterns. This helps in making the conversation sound more human-like and easier to understand.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;Your order number is &lt;break time="500ms"/&gt; 123456.<br>
                &lt;/speak&gt;
            </code>
        </div>
        <div class="benefit">
            <p class="benefit-title">Emphasis:</p>
            <p>SSML allows you to emphasize certain words or phrases, which can help in conveying important information more effectively.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;&lt;emphasis level="strong"&gt;Thank you&lt;/emphasis&gt; for your patience.<br>
                &lt;/speak&gt;
            </code>
        </div>
        <div class="benefit">
            <p class="benefit-title">Voice Selection:</p>
            <p>SSML enables the selection of different voices for different types of interactions. For example, a more formal voice can be used for official announcements, while a friendly voice can be used for customer greetings.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;&lt;voice name="en-US-JennyNeural"&gt;Welcome to our service center.&lt;/voice&gt;<br>
                &lt;/speak&gt;
            </code>
        </div>
        <div class="benefit">
            <p class="benefit-title">Pronunciation:</p>
            <p>You can use SSML to specify the pronunciation of certain words, ensuring that names, technical terms, or foreign words are pronounced correctly.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;The product name is &lt;phoneme alphabet="ipa" ph="ˈæpl"&gt;Apple&lt;/phoneme&gt;.<br>
                &lt;/speak&gt;
            </code>
        </div>
        <div class="benefit">
            <p class="benefit-title">Audio Effects:</p>
            <p>SSML supports the inclusion of audio effects, such as background music or sound effects, to enhance the overall customer experience.</p>
            <code>
                &lt;speak&gt;<br>
                &nbsp;&nbsp;&lt;audio src="sound_effect.mp3"&gt;Your call is important to us.&lt;/audio&gt;<br>
                &lt;/speak&gt;
            </code>
        </div>
    </div>
<style>
    .button-container {
        display: flex;
        gap: 10px;
    }
    .correct {
        background-color: green;
        color: white;
    }
    .incorrect {
        color: red;
    }
    .benefit {
            margin-bottom: 20px;
        }
        .benefit-title {
            font-weight: bold;
        }
        code {
            display: block;
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 5px;
            margin-top: 10px;
        }
</style>
<script>
    function markAnswer(button, isCorrect, resultId) {
        if (isCorrect) {
            button.classList.add('correct');
            document.getElementById(resultId).innerText = 'Correct Answer';
            document.getElementById(resultId).classList.remove('incorrect');
        } else {
            document.getElementById(resultId).innerText = 'Incorrect choice';
            document.getElementById(resultId).classList.add('incorrect');
        }
    }

 function toggleSolution(id) {
            var element = document.getElementById(id);
            if (element.style.display === "none") {
                element.style.display = "block";
            } else {
                element.style.display = "none";
            }
        }

</script>
