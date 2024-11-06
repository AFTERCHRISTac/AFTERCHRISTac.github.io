<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eclipse - Competitive Team</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400&display=swap');

        body {
            font-family: 'Orbitron', sans-serif;
            background: linear-gradient(145deg, #0d0d0d, #222);
            background-attachment: fixed;
            background-size: cover;
            color: #f3f3f3;
            margin: 0;
            padding: 0;
        }

        header {
            background: #111;
            color: #ffffff;
            padding: 20px;
            text-align: center;
            border-bottom: 2px solid #444;
        }

        header h1 {
            font-size: 3.5rem;
            text-transform: uppercase;
            margin: 0;
            color: #f05454;
            letter-spacing: 3px;
        }

        nav a {
            color: #f05454;
            margin: 0 15px;
            text-decoration: none;
            font-size: 1.1rem;
        }

        section {
            padding: 40px;
            text-align: center;
            background: rgba(25, 25, 25, 0.9);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.7);
        }

        .team-image {
            width: 80%;
            height: auto;
            max-width: 500px;
            border-radius: 20px;
            margin-top: 20px;
        }

        .team-description {
            font-size: 1.4rem;
            margin-top: 20px;
            line-height: 1.8;
            color: #e0e0e0;
        }

        .team-members, .achievements {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .member, .achievement {
            background: rgba(34, 34, 34, 0.8);
            border: 1px solid #333;
            border-radius: 10px;
            padding: 20px;
            margin: 10px;
            width: 250px;
            color: #d4d4d4;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }

        footer {
            background: #111;
            color: #ffffff;
            text-align: center;
            padding: 20px 0;
            border-top: 2px solid #444;
        }

        form input, form textarea {
            width: 300px;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #666;
            border-radius: 5px;
            background: #222;
            color: #f3f3f3;
        }

        form button {
            padding: 10px 20px;
            background-color: #f05454;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        form button:hover {
            background-color: #ff7675;
        }

        .social-media a {
            margin: 0 10px;
            text-decoration: none;
            color: #f05454;
        }
    </style>
</head>
<body>
    <header>
        <h1>Eclipse</h1>
        <p>A Premier Gorilla Tag Competitive Team</p>
        <nav>
            <a href="#about">About</a>
            <a href="#team">Team Members</a>
            <a href="#achievements">Achievements</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section id="about">
        <img src="background-image-placeholder.png" alt="Eclipse Team Image" class="team-image">
        <p class="team-description">Welcome to the official page of Eclipse, a high-performance competitive team dedicated to excellence and innovation in the Gorilla Tag arena. Join us as we aim for greatness and set new standards in gameplay!</p>
    </section>

    <section id="team">
        <h2>Meet the Team</h2>
        <div class="team-members">
            <div class="member">
                <h3>Member 1</h3>
                <p>Role: Captain</p>
                <p>Known for strategic vision and leadership.</p>
            </div>
            <div class="member">
                <h3>Member 2</h3>
                <p>Role: Sniper</p>
                <p>Exceptional precision and reflexes in every move.</p>
            </div>
            <div class="member">
                <h3>Member 3</h3>
                <p>Role: Support</p>
                <p>Always ready to assist and amplify the team's success.</p>
            </div>
            <div class="member">
                <h3>Member 4</h3>
                <p>Role: Scout</p>
                <p>Quick and agile, with an eye for detail.</p>
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
        <p>&copy; 2024 Eclipse Competitive Team. All Rights Reserved.</p>
    </footer>

    <script>
        function sendMessage(event) {
            event.preventDefault();

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
                    document.getElementById('contactForm').reset();
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
