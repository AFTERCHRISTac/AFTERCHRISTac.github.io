
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

        header, footer {
            background: #111;
            color: #ffffff;
            text-align: center;
            padding: 20px;
            border-bottom: 2px solid #444;
        }

        header h1 {
            font-size: 3.5rem;
            color: #f05454;
        }

        section, .expandable-section {
            padding: 20px;
            background: rgba(25, 25, 25, 0.9);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.7);
            display: none;
        }

        .button-container {
            text-align: center;
            margin-top: 40px;
        }

        .expand-button {
            padding: 10px 20px;
            background-color: #f05454;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }

        .expand-button:hover {
            background-color: #ff7675;
        }
    </style>
</head>
<body>
    <header>
        <h1>Eclipse</h1>
        <p>A Premier Gorilla Tag Competitive Team</p>
    </header>

    <section id="about">
        <p>Welcome to Eclipse, a high-performance team in Gorilla Tag.</p>
    </section>

    <!-- Button Container for expandable sections -->
    <div class="button-container">
        <button class="expand-button" onclick="toggleSection('mission')">Our Mission</button>
        <button class="expand-button" onclick="toggleSection('schedule')">Training Schedule</button>
        <button class="expand-button" onclick="toggleSection('tournaments')">Upcoming Tournaments</button>
        <button class="expand-button" onclick="toggleSection('coaches')">Contact Coaches</button>
    </div>

    <!-- Expandable Sections -->
    <section id="mission" class="expandable-section">
        <h2>Our Mission</h2>
        <p>To push the limits of competitive play, representing Eclipse with excellence.</p>
    </section>

    <section id="schedule" class="expandable-section">
        <h2>Training Schedule</h2>
        <p>Our team trains every Wednesday and Friday at 6 PM EST.</p>
    </section>

    <section id="tournaments" class="expandable-section">
        <h2>Upcoming Tournaments</h2>
        <p>Catch us in the next Ultimate COMP Gorilla Tag Tournament on November 15th!</p>
    </section>

    <section id="coaches" class="expandable-section">
        <h2>Contact Coaches</h2>
        <p>Reach out to our coaches via email at coaches@eclipse.com or on Discord.</p>
    </section>

    <footer>
        <p>&copy; 2024 Eclipse Competitive Team. All Rights Reserved.</p>
    </footer>

    <script>
        function toggleSection(id) {
            const section = document.getElementById(id);
            section.style.display = section.style.display === "none" || section.style.display === "" ? "block" : "none";
        }
    </script>
</body>
</html>
