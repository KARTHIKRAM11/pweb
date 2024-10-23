PERS<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Interactive Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h2 {
            margin-top: 0;
        }
        #chatbox {
            border: 1px solid #ccc;
            height: 300px;
            overflow-y: auto;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            background-color: #f9f9f9;
        }
        .message {
            margin: 10px 0;
        }
        .user {
            text-align: right;
            color: blue;
        }
        .bot {
            text-align: left;
            color: green;
        }
        input[type="text"] {
            width: calc(100% - 20px);
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="button"] {
            padding: 10px;
            border: none;
            background-color: #5cb85c;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="button"]:hover {
            background-color: #4cae4c;
        }
        section {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

<header>
    <h1>Welcome to My Personal Website</h1>
</header>

<div class="container">
    <section>
        <h2>About Me</h2>
        <p><strong>Objective:</strong> I am S.Karthikram. I am a highly determined and hardworking person, with a passion towards technologies. I'm more inclined towards upcoming technologies and I work hard with perseverance to achieve my goals.</p>
        <p><strong>Skills:</strong> Java, C, C++, QGIS Software, Problem Solving.</p>
        <p><strong>Achievements:</strong> Completed AI certifications, won Olympiads and science quiz competitions.</p>
    </section>

    <section>
        <h2>Chat with Me</h2>
        <div id="chatbox"></div>
        <input type="text" id="userInput" placeholder="Type your message here...">
        <input type="button" value="Send" onclick="sendMessage()">
    </section>
</div>

<script>
    function sendMessage() {
        const userInput = document.getElementById('userInput').value;
        if (!userInput) return;

        const chatbox = document.getElementById('chatbox');
        chatbox.innerHTML += `<div class="message user">${userInput}</div>`;
        document.getElementById('userInput').value = '';

        setTimeout(() => {
            const botResponse = getBotResponse(userInput);
            chatbox.innerHTML += `<div class="message bot">${botResponse}</div>`;
            chatbox.scrollTop = chatbox.scrollHeight;
        }, 500);
    }

    function getBotResponse(input) {
        const responses = {
            "Hi": "Hello! How can I assist you today?",
            "How are you ?": "I'm just a program, but I'm here to help you!",
            "What can you do ?": "I can answer your questions and chat with you!",
            "Bye": "Goodbye! Have a great day!",
            "Skills": "My skills include Java, C, C++, QGIS Software, and Problem Solving.",
            "Objective": "My objective is to work hard towards achieving my goals in technology.",
            "Who created you ?": "S.Karthikram."
        };
        return responses[input.toLowerCase()] || "Sorry, I didn't understand that.";
    }
</script>

</body>
</html>
ONAL WEBPAGE
