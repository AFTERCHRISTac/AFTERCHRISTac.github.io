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
            background-image: url('C:/Users/mason/Downloads/family.png');
            background-size: cover; /* Makes the background image cover the entire area */
            background-position: center; /* Centers the background image */
            color: #fff; /* Change text color to white for better contrast */
            margin: 0;
            padding: 0;
        }

        header {
            background-color: rgba(51, 51, 51, 0.7); /* Semi-transparent background */
            color: #fff;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 3rem;
        }

        nav {
            margin: 20px 0;
        }

        nav a {
            color: #fff;
            margin: 0 15px;
            text-decoration: none;
        }

        section {
            padding: 40px;
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6); /* Semi-transparent background for readability */
            margin: 20px;
            border-radius: 10px; /* Rounded corners */
        }

        section img {
            width: 300px;
            height: auto;
            border-radius: 50%;
            margin-top: 20px;
        }

        section p {
            font-size: 1.5rem;
            margin-top: 20px;
            line-height: 1.6;
        }

        .team-members, .achievements {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .member, .achievement {
            background: rgba(255, 255, 255, 0.9); /* Semi-transparent white */
            border: 1px solid #ddd;
            border-radius: 10px;
            padding: 20px;
            margin: 10px;
            width: 250px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        footer {
            background-color: rgba(51, 51, 51, 0.7); /* Semi-transparent background */
            color: #fff;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }

        form {
            margin-top: 30px;
        }

        form input, form textarea {
            width: 300px;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        form button {
            padding: 10px 20px;
            background-color: #333;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
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
        <img src="C:/Users/mason/Downloads/family.png" alt="AFTER CHRIST Team Image">
        <p>Welcome to the official page of AFTER CHRIST (AC), a high-profile competitive team. We strive for excellence and have a passion for pushing the boundaries of competitive Gorilla Tag. Join us as we aim for the top!</p>
    </section>

    <section id="team">
        <h2>Meet the Team</h2>
        <div class="team-members">
            <div class="member">
                <h3>Member 1</h3>
                <p>Role: Captain</p>
                <p>Bio: A dedicated player with a love for strategy and teamwork.</p>
            </div>
            <div class="member">
                <h3>Member 2</h3>
                <p>Role: Sniper</p>
                <p>Bio: Known for precise shots and quick reflexes.</p>
            </div>
            <div class="member">
                <h3>Member 3</h3>
                <p>Role: Support</p>
                <p>Bio: Always there to assist teammates and strategize.</p>
            </div>
            <div class="member">
                <h3>Member 4</h3>
                <p>Role: Scout</p>
                <p>Bio: Fast and agile, perfect for gathering information.</p>
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
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
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
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;

            const webhookURL = 'https://discord.com/api/webhooks/1297315112167931937/t7-Lwto-L2ONP_dwdHZ-yyVyrE9_-0PB5RJkT4xOyc9itlgWUYNAhNLbl23MrgXfpYia';

            const payload = {
                content: `New message from ${name} (${email}): ${message}`
            };

            fetch(webhookURL, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(payload)
            })
            .then(response => {
                if (response.ok) {
                    alert('Message sent successfully!');
                    document.getElementById('contactForm').reset(); // Reset the form
                } else {
                    alert('Error sending message. Please try again later.');
                }
            })
            .catch(error => {
                console.error('Error:', error);
                alert('Error sending message. Please try again later.');
            });
        }
    </script>
</body>
</html>
