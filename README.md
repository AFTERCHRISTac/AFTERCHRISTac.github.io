<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AFTER CHRIST - Competitive Team</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Daydream:wght@400&display=swap');

        body {
            font-family: 'Daydream', cursive;
            background: linear-gradient(to bottom, black, gray);
            color: #fff;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: rgba(0, 0, 0, 0.7);
            color: #fff;
            padding: 20px;
            text-align: center;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
        }

        header h1 {
            margin: 0;
            font-size: 3rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        nav {
            margin: 20px 0;
        }

        nav a {
            color: #fff;
            margin: 0 15px;
            text-decoration: none;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.7);
        }

        section {
            padding: 40px;
            text-align: center;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            margin: 20px;
            box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.5);
        }

        section p {
            font-size: 1.5rem;
            margin-top: 20px;
            line-height: 1.6;
        }

        footer {
            background-color: rgba(0, 0, 0, 0.7);
            color: #fff;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
            box-shadow: 0px -4px 10px rgba(0, 0, 0, 0.5);
        }

        form {
            margin-top: 30px;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
            background-color: rgba(255, 255, 255, 0.1);
        }

        form input, form select {
            width: 90%;
            max-width: 300px;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.2);
            color: #fff;
            box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.3);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        form input:hover, form select:hover {
            transform: scale(1.05);
            box-shadow: 0px 6px 15px rgba(0, 0, 0, 0.7);
        }

        form button {
            padding: 10px 20px;
            background-color: #333;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 90%;
            max-width: 300px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
        }

        form button:hover {
            background-color: #555;
        }

        .social-media {
            margin-top: 20px;
        }

        .social-media a {
            margin: 0 10px;
            text-decoration: none;
            color: #fff;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.7);
        }
    </style>
</head>
<body>
    <header>
        <h1>AFTER CHRIST</h1>
        <p>(AC) - A High Pro Gorilla Tag Competitive Team</p>
        <nav>
            <a href="#about">About</a>
            <a href="#team">Team Members</a>
            <a href="#achievements">Achievements</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section id="about">
        <p>Welcome to the official page of AFTER CHRIST (AC), a high-profile competitive team. We strive for excellence and have a passion for pushing the boundaries of competitive Gorilla Tag. Join us as we aim for the top!</p>
    </section>

    <section id="create-account">
        <h2>Create an Account</h2>
        <form id="accountForm" onsubmit="createAccount(event)">
            <input type="text" id="username" placeholder="Choose a Username" required>
            <input type="password" id="password" placeholder="Enter a Password" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <button type="submit">Create Account</button>
        </form>
    </section>

    <section id="team">
        <h2>Meet the Team</h2>
        <div class="team-members">
            <div class="member">
                <h3>CAPTAIN</h3>
                <p>A person in charge of the team, managing, promoting, and helping new people.</p>
            </div>
            <div class="member">
                <h3>TEAM PLAYER</h3>
                <p>A player that participates in scrims and team practices.</p>
            </div>
            <div class="member">
                <h3>OFFICIAL PLAYER</h3>
                <p>Plays in official scrims and in events like GTC, CGT, etc.</p>
            </div>
            <div class="member">
                <h3>SCOUT</h3>
                <p>A player that helps look for new official players and team players.</p>
            </div>
            <div class="member">
                <h3>CO-CAPTAIN</h3>
                <p>Helps manage the team and assists the captain.</p>
            </div>
        </div>
    </section>

    <section id="achievements">
        <h2>Our Achievements</h2>
        <div class="achievements">
            <div class="achievement">
                <h3><strong>Coming Soon</strong></h3>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm" onsubmit="sendMessage(event)">
            <input type="text" id="name" placeholder="Your Discord Username" required>
            <select id="role" required>
                <option value="" disabled selected>Select Your Role</option>
                <option value="Team Player">Team Player</option>
                <option value="Official Player">Official Player</option>
                <option value="Scout">Scout</option>
            </select>
            <textarea id="message" rows="4" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
        <div class="social-media">
            <h3>Follow Us</h3>
            <a href="#">Facebook</a>
            <a href="#">Twitter</a>
            <a href="#">Instagram</a>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 AFTER CHRIST Competitive Team. All Rights Reserved.</p>
    </footer>

    <script>
        function sendMessage(event) {
            event.preventDefault(); // Prevent the form from submitting normally

            const name = document.getElementById('name').value;
            const role = document.getElementById('role').value;
            const message = document.getElementById('message').value;

            const webhookURL = 'https://discord.com/api/webhooks/1297315112167931937/t7-Lwto-L2ONP_dwdHZ-yyVyrE9_-0PB5RJkT4xOyc9itlgWUYNAhNLbl23MrgXfpYia';

            const payload = {
                content: `New message from ${name} (Role: ${role}): ${message}`
            };

            fetch(webhookURL, {
                method: 'POST',
                headers: {
                    'Content-Type': '
