<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fragene</title>
    <style>
        /* CSS-Stile für die Website */
        body {
            background-color: #080808; /* Helle Schwarze Hintergrundfarbe */
            text-align: center; /* Zentrierter Text */
            font-size: 24px; /* Größere Schriftgröße */
            color: white; /* Weiße Schriftfarbe */
            margin-top: 100px; /* Abstand von oben */
            animation: backgroundAnimation 10s infinite; /* Hintergrundanimation */
            position: relative; /* Relative Position für die Platzierung der Punkte */
        }

        h1 {
            font-size: 36px; /* Größere Schriftgröße für die Überschrift */
            margin: 20px 0; /* Abstand über und unter der Überschrift */
        }

        .button-container {
            display: flex;
            justify-content: center;
            margin-top: 50px; /* Abstand von oben für Button-Container */
        }

        button {
            font-size: 24px; /* Größere Schriftgröße für die Buttons */
            padding: 10px 30px; /* Zusätzlicher Platz um den Text in den Buttons */
            margin: 10px 20px; /* Abstand zwischen den Buttons (horizontal und vertikal) */
            border: none; /* Keine Rahmen um die Buttons */
            cursor: pointer; /* Zeige Handcursor beim Überfahren der Buttons */
            background-color: #2a2a2a; /* Dunklerer Hintergrund für Buttons */
            color: white; /* Weiße Schriftfarbe für Buttons */
            transition: background-color 0.3s, transform 0.2s; /* Animationen für Hintergrundfarbe und Transformation */
        }

        #jaButton {
            background-color: #28a745; /* Angenehmes Grün für den "Ja"-Button */
        }

        #neinButton {
            background-color: #dc3545; /* Entspanntes Rot für den "Nein"-Button */
        }

        button:hover {
            background-color: #0056b3; /* Dunklere Blaue Hintergrundfarbe beim Überfahren der Buttons */
            transform: scale(1.05); /* Vergrößere den Button beim Überfahren */
        }

        /* CSS für die Hintergrundanimation */
        @keyframes backgroundAnimation {
            0% {
                background-position: 0 0;
            }
            100% {
                background-position: 100% 0;
            }
        }

        /* CSS für die kleinen weißen Punkte */
        body::before {
            content: "";
            position: absolute;
            top: 10px;
            left: 10px;
            width: 5px;
            height: 5px;
            background-color: white;
            border-radius: 50%;
            animation: dotsAnimation 4s infinite;
        }

        @keyframes dotsAnimation {
            0%, 100% {
                transform: translate(0, 0);
            }
            25% {
                transform: translate(10px, 10px);
            }
            50% {
                transform: translate(0, 20px);
            }
            75% {
                transform: translate(-10px, 10px);
            }
        }
    </style>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <div class="button-container">
        <button id="jaButton">Ja</button>
        <button id="neinButton">Nein</button>
    </div>

    <script>
        // JavaScript-Code zur Interaktion mit den Buttons
        document.getElementById('jaButton').addEventListener('click', function() {
            // JavaScript-Code, um Gesamtpunkte zu vergeben und zu speichern
            let punkte = parseInt(localStorage.getItem("punkte")) || 0; // Gesamtpunkte aus dem Local Storage laden oder auf 0 setzen
            punkte += 10;
            localStorage.setItem("punkte", punkte); // Gesamtpunkte in den Local Storage speichern

            // JavaScript-Code, um Punktzahl der erledigten Aufgaben zu vergeben und zu speichern
            let ErlAuf = parseInt(localStorage.getItem("ErlAuf")) || 0; // Punktzahl der erledigten Aufgaben aus dem Local Storage laden oder auf 0 setzen
            ErlAuf += 1;
            localStorage.setItem("ErlAuf", ErlAuf); // Punktzahl der erledigten Aufgaben in den Local Storage speichern

            // Weiterleitung zur Statistikseite mit JavaScript
            window.location.href = 'https://leon22221.github.io/Site-L/?status=completed';
        });

       document.getElementById('neinButton').addEventListener('click', function() {
            // JavaScript-Code, um Free Tickets zu vergeben und zu speichern
            let freeTickets = parseInt(localStorage.getItem("freeTickets")) || 0; // Free Tickets aus dem Local Storage laden oder auf 0 setzen
            freeTickets += 1;
            localStorage.setItem("freeTickets", freeTickets); // Free Tickets in den Local Storage speichern

            // Weiterleitung zur Statistikseite mit dem Hinweis auf ein Free Ticket
            window.location.href = 'https://leon22221.github.io/Site-L/?status=not_completed';
        });
    </script>
</body>
</html>
