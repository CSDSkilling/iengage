---
layout: default
title:  "Sentinel for Cyber Threats"
category: "Gamification"
sub-category: "Security, Compliance and Identity"
courses: [SC-200, AZ-500]
---

# Sentinel for Cyber Threats

## Introduction:
A mid-sized company, Contoso Retail, recently migrated its IT infrastructure to Azure. Set up a small SOC  team.  They are concerned about increasing cyber threats, especially phishing attacks targeting their employees. They decided to implement Microsoft Sentinel to enhance their security posture.

## Listen to conversation between Alice and Bob about the recent phishing attack

<iframe class="smart-player-embed-iframe" id="embeddedSmartPlayerInstance" src="/iengage/project-files/gamification/Security, Compliance and Identity/videos/sentinel/sentinel_player.html?embedIFrameId=embeddedSmartPlayerInstance" width="1024" height="600" scrolling="no" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .knowledge-check {
            margin-top: 50px;
        }
        .knowledge-check-question {
            margin-bottom: 20px;
        }
        .correct {
            color: green;
        }
        .incorrect {
            color: red;
        }
    </style>
</head>
<body>

    <div class="knowledge-check">
        <h2>Knowledge Check</h2>
        <form id="knowledgeCheckForm">
            <div class="knowledge-check-question">
                <p>1. Alice received a phishing email during a drill. What tool does Bob mention their organization uses to tackle phishing issues?</p>
                <label><input type="radio" name="question1" value="A">A) Firewalls</label><br>
                <label><input type="radio" name="question1" value="B">B) Microsoft Sentinel</label><br>
                <label><input type="radio" name="question1" value="C">C) Antivirus Software </label><br>
                <label><input type="radio" name="question1" value="D">D) Email Filters</label>
            </div>
            <div class="knowledge-check-question">
                <p>2. Bob explains that the first step in using Microsoft Sentinel is to get all security data into one place. Which feature of Sentinel is used for this purpose?</p>
                <label><input type="radio" name="question2" value="A">A) Playbooks</label><br>
                <label><input type="radio" name="question2" value="B">B) Analytics Rules</label><br>
                <label><input type="radio" name="question2" value="C">C) Data Connectors</label><br>
                <label><input type="radio" name="question2" value="D">D) Workbooks</label>
            </div>
            <div class="knowledge-check-question">
                <p>3. In the scenario, Bob mentions using Analytics Rules to detect phishing attempts. What specific keywords do these rules look for?</p>
                <label><input type="radio" name="question3" value="A">A) "Congratulations," "You won"</label><br>
                <label><input type="radio" name="question3" value="B">B) "Urgent," "Password reset"</label><br>
                <label><input type="radio" name="question3" value="C">C) "Free," "Gift voucher"</label><br>
                <label><input type="radio" name="question3" value="D">D) "Alert," "Security breach"</label>
            </div>
            <div class="knowledge-check-question">
                <p>4. Bob describes a feature that checks for Correlation in suspicious activities. Which of the following scenarios would raise a red flag according to this feature?</p>
                <label><input type="radio" name="question4" value="A">A) A user receives a suspicious email and then immediately has a failed login attempt.</label><br>
                <label><input type="radio" name="question4" value="B">B) A user changes their password successfully.</label><br>
                <label><input type="radio" name="question4" value="C">C) A user logs in from their usual location.</label><br>
                <label><input type="radio" name="question4" value="D">D) A user receives a congratulatory email.</label>
            </div>
            <div class="knowledge-check-question">
                <p>5. Once Sentinel detects a phishing attempt, what automated response does Bob say their organization has set up using Playbooks?</p>
                <label><input type="radio" name="question5" value="A">A) Sending a warning email to the user</label><br>
                <label><input type="radio" name="question5" value="B">B) Blocking the phishing sender, resetting the affected user's password, and alerting the security team</label><br>
                <label><input type="radio" name="question5" value="C">C) Logging the incident for future reference</label><br>
                <label><input type="radio" name="question5" value="D">D) Manually investigating the incident</label>
            </div>
            <div class="knowledge-check-question">
                <p>6. Bob mentions using Kusto Query Language (KQL) for proactive threat hunting. What is the primary purpose of using KQL in Microsoft Sentinel?</p>
                <label><input type="radio" name="question6" value="A">A) Generating reports</label><br>
                <label><input type="radio" name="question6" value="B">B) Automating responses</label><br>
                <label><input type="radio" name="question6" value="C">C) Searching for suspicious patterns and threats</label><br>
                <label><input type="radio" name="question6" value="D">D) Visualizing data</label>
            </div>
            <div class="knowledge-check-question">
                <p>7. To keep track of security information, Bob says they built Workbooks. What do these Workbooks provide?</p>
                <label><input type="radio" name="question7" value="A">A) Automated responses to threats</label><br>
                <label><input type="radio" name="question7" value="B">B) Interactive visualizations of security data and key metrics</label><br>
                <label><input type="radio" name="question7" value="C">C) Alerts for suspicious activities</label><br>
                <label><input type="radio" name="question7" value="D">D) Data ingestion from various sources</label>
            </div>
            <button type="button" onclick="checkAnswers()">Submit</button>
        </form>
        <div id="results"></div>
    </div>

    <script>
        function checkAnswers() {
            const answers = {
                question1: 'B',
                question2: 'C',
                question3: 'B',
                question4: 'A',
                question5: 'B',
                question6: 'C',
                question7: 'B'
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
                    questionElement.classList.add('correct');
                } else if (selected) {
                    selected.parentElement.classList.add('incorrect');
                    questionElement.classList.add('correct');
                } else {
                    questionElement.classList.add('correct');
                }
            }

            results.innerHTML = `You got ${score} out of ${Object.keys(answers).length} correct.`;
        }
    </script>
</body>
</html>
