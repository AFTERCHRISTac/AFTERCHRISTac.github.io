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

        section {
            padding: 40px;
            text-align: center;
            background: rgba(25, 25, 25, 0.9);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.7);
        }

        .more-button {
            padding: 10px 20px;
            background-color: #f05454;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1rem;
            margin-top: 10px;
        }

        .more-button:hover {
            background-color: #ff7675;
        }

        .more-section {
            display: none;
            margin-top: 20px;
            color: #f3f3f3;
            background: rgba(34, 34, 34, 0.9);
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Eclipse</h1>
        <p>Unleashing Ultimate Talent in Gorilla Tag Competitions</p>
    </header>

    <!-- About Section -->
    <section id="about">
        <h2>About Eclipse</h2>
        <p>We’re dedicated to mastering Gorilla Tag, bringing you exhilarating gameplay and unmatched skill.</p>
        <button class="more-button" onclick="toggleSection('aboutHistory')">Our History</button>
        <div id="aboutHistory" class="more-section">
            <p>Formed by passionate players, Eclipse has quickly risen through the ranks, becoming a feared competitor.</p>
        </div>
        <button class="more-button" onclick="toggleSection('philosophy')">Our Philosophy</button>
        <div id="philosophy" class="more-section">
            <p>Driven by a commitment to excellence and teamwork, we believe in playing fairly and mastering our skills to lead the field.</p>
        </div>
    </section>

    <!-- Achievements Section -->
    <section id="achievements">
        <h2>Our Achievements</h2>
        <button class="more-button" onclick="toggleSection('comingSoon')">Show More Achievements</button>
        <div id="comingSoon" class="more-section">
            <p><strong>Coming Soon:</strong> Stay tuned for our upcoming awards and accomplishments as we continue to dominate the arena.</p>
        </div>
    </section>

    <!-- Meet the Team Section -->
    <section id="team">
        <h2>Meet the Team</h2>
        <p>Our team is composed of skilled individuals, each bringing unique strengths to every match.</p>
        <button class="more-button" onclick="toggleSection('roster')">Roster</button>
        <div id="roster" class="more-section">
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
        <button class="more-button" onclick="toggleSection('roles')">Our Key Roles</button>
        <div id="roles" class="more-section">
            <div><strong>Team Manager:</strong> Coordinates events and ensures smooth operations.</div>
            <div><strong>Scrim Manager:</strong> Manages scrimmages and practice sessions.</div>
            <div><strong>Referee:</strong> Ensures adherence to fair play.</div>
            <div><strong>Caster:</strong> Provides live commentary during matches.</div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm" onsubmit="sendMessage(event)">
            <input type="text" id="name" placeholder="Your Name" required>
            <textarea id="message" rows="4" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <script>
        function toggleSection(sectionId) {
            const section = document.getElementById(sectionId);
            section.style.display = section.style.display === 'block' ? 'none' : 'block';
        }

        function sendMessage(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const message = document.getElementById('message').value;
            const webhookURL = 'https://discord.com/api/webhooks/1303555595907108884/QZSxuSDug616xvyF2dTHziooRjCSk7twoTFod5-6qKVqGUVQwlmNdbJ_kBzm3Cg-Nok1';

            const payload = { content: `New message from ${name}: ${message}` };

            fetch(webhookURL, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
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
