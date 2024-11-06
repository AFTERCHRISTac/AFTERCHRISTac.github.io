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
            position: relative;
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

        .more-section, .scrim-schedule-section {
            display: none;
            margin-top: 20px;
            color: #f3f3f3;
            background: rgba(34, 34, 34, 0.9);
            padding: 20px;
            border-radius: 10px;
        }

        .more-button, .scrim-schedule-button {
            padding: 10px 20px;
            background-color: #f05454;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1rem;
            margin-top: 10px;
        }

        .more-button:hover, .scrim-schedule-button:hover {
            background-color: #ff7675;
        }

        .achievement-toggle {
            cursor: pointer;
            color: #f05454;
            font-weight: bold;
            font-size: 1.2rem;
        }

        .achievement-content {
            display: none;
            margin-top: 10px;
            color: #e0e0e0;
        }

        .achievement:hover .achievement-content {
            display: block;
        }

        .achievement-section {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
        }

        .achievement-category {
            width: 30%;
            background: rgba(50, 50, 50, 0.8);
            padding: 20px;
            border-radius: 10px;
            margin: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }

        .achievement-category h3 {
            text-align: center;
            font-size: 1.5rem;
            color: #f05454;
        }

        .achievement-item {
            cursor: pointer;
            margin: 10px 0;
            text-align: center;
            color: #f05454;
            font-weight: bold;
            font-size: 1.2rem;
        }

        .achievement-item:hover {
            color: #ff7675;
        }

        .achievement-item p {
            display: none;
            color: #e0e0e0;
        }

        .achievement-item.active p {
            display: block;
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
                <h3>Official Member</h3>
                <p>Part of our dedicated competitive roster.</p>
            </div>
            <div class="member">
                <h3>Team Manager</h3>
                <p>Oversees operations and coordinates team activities.</p>
            </div>
            <div class="member">
                <h3>Scrim Manager</h3>
                <p>Organizes and manages practice sessions.</p>
            </div>
            <div class="member">
                <h3>Referee</h3>
                <p>Ensures fair play and upholds team rules.</p>
            </div>
            <div class="member">
                <h3>Caster</h3>
                <p>Provides engaging commentary during matches.</p>
            </div>
        </div>
        <button class="more-button" onclick="toggleMore()">More</button>
        <div class="more-section" id="moreContent">
            <h2>Leagues & Roster</h2>
            <p><strong>League:</strong> Ultimate COMP Gorilla Tag</p>
            <h3>Roster</h3>
            <ul>
                <li>@errorxm</li>
                <li>@𝓩𝓮𝓽𝓪✞</li>
                <li>@AC MNM</li>
                <li>@Chikune</li>
                <li>@no name</li>
                <li>@vision brought pizza for you all</li>
                <li>@Beats</li>
                <li>@D1V8IN</li>
                <li>@Ⓑ</li>
                <li>@✦CARTIFE!NV4MP✦</li>
            </ul>
        </div>
    </section>

    <section id="achievements">
        <h2>Our Achievements</h2>
        <div class="achievement-section">
            <!-- Player Achievement -->
            <div class="achievement-category">
                <h3>Player</h3>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>Player 1</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>Player 2</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
            </div>
            <!-- Team Achievement -->
            <div class="achievement-category">
                <h3>Team</h3>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>Team Achievement 1</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>Team Achievement 2</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
            </div>
            <!-- League Achievement -->
            <div class="achievement-category">
                <h3>League</h3>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>League Achievement 1</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
                <div class="achievement-item" onclick="toggleAchievementContent(this)">
                    <p>League Achievement 2</p>
                    <p class="achievement-content">Coming Soon</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm" onsubmit="sendMessage(event)">
            <input type="text" id="name" placeholder="Your Name" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Eclipse - All Rights Reserved.</p>
    </footer>

    <script>
        function toggleMore() {
            const moreSection = document.getElementById('moreContent');
            moreSection.style.display = (moreSection.style.display === 'none' || moreSection.style.display === '') ? 'block' : 'none';
        }

        function toggleAchievementContent(element) {
            element.classList.toggle('active');
        }

        function sendMessage(event) {
            event.preventDefault();

            const name = document.getElementById('name').value;
            const message = document.getElementById('message').value;
            const webhookUrl = "https://discord.com/api/webhooks/1303555595907108884/QZSxuSDug616xvyF2dTHziooRjCSk7twoTFod5-6qKVqGUVQwlmNdbJ_kBzm3Cg-Nok1";

            fetch(webhookUrl, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    content: `Name: ${name}\nMessage: ${message}`
                })
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
