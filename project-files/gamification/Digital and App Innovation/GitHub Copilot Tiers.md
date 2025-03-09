---
layout: default
title:  "GitHub Copilot Plans"
category: "Gamification"
sub-category: "Digital and App Innovation"
courses: [AZ-2007]
---

# Boosting Productivity with GitHub Copilot: Amit and Priya's Journey

## Introduction:
In this story, we follow two developers, Amit and Priya, as they navigate the challenges of maintaining productivity in their coding tasks. Amit is feeling overwhelmed with his workload, and Priya introduces him to GitHub Copilot, an AI-powered coding assistant. Through their conversation, they explore the features of GitHub Copilot Free and GitHub Copilot Enterprise, and discuss how upgrading to the Enterprise plan can significantly enhance their team's productivity. Join Amit and Priya on their journey to discover the benefits of GitHub Copilot and how it can transform their development process.

## Interactive Video 

After listening to the video, you will take up the quizzes.

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Digital%20and%20App%20Innovation/videos/githubplan/GitHub_player.html?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

<div class="knowledge-check" style="margin-top: 50px;">
    <h2>Knowledge Check</h2>
    <form id="knowledgeCheckForm">
        <div class="knowledge-check-question" style="margin-bottom: 20px;">
            <p>Question 1: What is GitHub Copilot Free?</p>
            <label><input type="radio" name="question1" value="A">A. An AI-powered coding assistant available to individual users with limited features.</label><br>
            <label><input type="radio" name="question1" value="B">B. A premium version of GitHub Copilot with advanced features.</label><br>
            <label><input type="radio" name="question1" value="C">C. A tool for managing pull requests in GitHub.</label><br>
            <label><input type="radio" name="question1" value="D">D. A chat interface for asking coding-related questions.</label>
        </div>
        <div class="knowledge-check-question" style="margin-bottom: 20px;">
            <p>Question 2: What is the first step to upgrade to GitHub Copilot Enterprise?</p>
            <label><input type="radio" name="question2" value="A">A. Purchase Copilot Enterprise directly.</label><br>
            <label><input type="radio" name="question2" value="B">B. Sign in as an enterprise admin.</label><br>
            <label><input type="radio" name="question2" value="C">C. Start a free 30-day trial.</label><br>
            <label><input type="radio" name="question2" value="D">D. Assign Copilot Enterprise to individual organizations.</label>
        </div>
        <div class="knowledge-check-question" style="margin-bottom: 20px;">
            <p>Question 3: Which feature is included in GitHub Copilot Enterprise but not in GitHub Copilot Free?</p>
            <label><input type="radio" name="question3" value="A">A. Code completion in IDEs.</label><br>
            <label><input type="radio" name="question3" value="B">B. Copilot Chat.</label><br>
            <label><input type="radio" name="question3" value="C">C. Copilot Pull Request Summaries.</label><br>
            <label><input type="radio" name="question3" value="D">D. Usage limits of up to 2000 code completions per month.</label>
        </div>
        <div class="knowledge-check-question" style="margin-bottom: 20px;">
            <p>Question 4: What is the usage limit for Copilot Chat messages per month in GitHub Copilot Free?</p>
            <label><input type="radio" name="question4" value="A">A. 100 messages</label><br>
            <label><input type="radio" name="question4" value="B">B. 50 messages</label><br>
            <label><input type="radio" name="question4" value="C">C. 200 messages</label><br>
            <label><input type="radio" name="question4" value="D">D. 500 messages</label>
        </div>            
        <div class="knowledge-check-question" style="margin-bottom: 20px;">
            <p>Question 5: Which feature provides AI-generated code review suggestions in GitHub Copilot Enterprise?</p>
            <label><input type="radio" name="question5" value="A">A. Copilot Workspace</label><br>
            <label><input type="radio" name="question5" value="B">B. Copilot Text Completion</label><br>
            <label><input type="radio" name="question5" value="C">C. Copilot Extensions</label><br>
            <label><input type="radio" name="question5" value="D">D. Copilot Code Review</label>
        </div>               
        <button type="button" onclick="checkAnswers()">Submit</button>
    </form>
    <div id="results"></div>
</div>

<script>
    function checkAnswers() {
        const answers = {
            question1: 'A',
            question2: 'B',
            question3: 'C',
            question4: 'B',
            question5: 'D'
        };

        let score = 0;
        const form = document.getElementById('knowledgeCheckForm');
        const results = document.getElementById('results');
        results.innerHTML = '';

        for (const [question, correctAnswer] of Object.entries(answers)) {
            const selected = form.querySelector(`input[name="${question}"]:checked`);
            const questionElement = form.querySelector(`input[name="${question}"][value="${correctAnswer}"]`).parentElement;
            if (selected && selected.value === correctAnswer) {
                score++;
                questionElement.style.color = 'green';
            } else if (selected) {
                selected.parentElement.style.color = 'red';
                questionElement.style.color = 'green';
            } else {
                questionElement.style.color = 'green';
            }
        }

        results.innerHTML = `You got ${score} out of ${Object.keys(answers).length} correct.`;
    }
</script>
