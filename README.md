<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fragene</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button id="jaButton">Ja</button>
    <button id="neinButton">Nein</button>

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
