<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gorilla Tag Comp Teams</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
        }
        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            text-transform: uppercase;
        }
        nav a:hover {
            background-color: #555;
        }
        .container {
            padding: 20px;
        }
        .team-section, .matches-section, .contact-section {
            margin-bottom: 40px;
        }
        .team-section h2, .matches-section h2, .contact-section h2 {
            border-bottom: 2px solid #333;
            padding-bottom: 10px;
        }
        .team-members, .matches-list {
            list-style-type: none;
            padding: 0;
        }
        .team-members li, .matches-list li {
            background-color: white;
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ddd;
            box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>

<header>
    <h1>Gorilla Tag Competitive Teams</h1>
</header>

<nav>
    <a href="#team">Team</a>
    <a href="#matches">Matches</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container">
    <!-- Team Section -->
    <section id="team" class="team-section">
        <h2>Meet the Team</h2>
        <ul class="team-members">
            <li><strong>Player 1</strong> - Team Leader</li>
            <li><strong>Player 2</strong> - Offensive</li>
            <li><strong>Player 3</strong> - Defensive</li>
            <li><strong>Player 4</strong> - Support</li>
        </ul>
    </section>

    <!-- Matches Section -->
    <section id="matches" class="matches-section">
        <h2>Upcoming Matches</h2>
        <ul class="matches-list">
            <li><strong>Match 1:</strong> Team A vs. Team B - Date: 10/25/2024</li>
            <li><strong>Match 2:</strong> Team A vs. Team C - Date: 11/01/2024</li>
            <li><strong>Match 3:</strong> Team A vs. Team D - Date: 11/08/2024</li>
        </ul>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact-section">
        <h2>Contact Us</h2>
        <form action="submit_contact_form.php" method="POST">
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email" required><br><br>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message" rows="5" required></textarea><br><br>
            <input type="submit" value="Submit">
        </form>
    </section>
</div>

<footer>
    <p>&copy; 2024 Gorilla Tag Comp Teams. All rights reserved.</p>
</footer>

</body>
</html>
