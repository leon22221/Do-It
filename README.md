<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fragene</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button id="jaButton" onclick="window.location.href = 'https://leon22221.github.io/Site-L/';">Ja</button>
    <button id="neinButton">Nein</button>

    <script>
        // JavaScript-Code zur Interaktion mit den Buttons
        document.getElementById('jaButton').addEventListener('click', function() {
            // JavaScript-Code, um Punkte zu vergeben und zu speichern
            let punkte = parseInt(localStorage.getItem("punkte")) || 0; // Punkte aus dem Local Storage laden oder auf 0 setzen
            punkte += 10;
            localStorage.setItem("punkte", punkte); // Punkte in den Local Storage speichern
            document.getElementById("punkte").textContent = punkte; // Aktualisiere die Punkteanzeige
            localStorage.setItem("punkte", 0); // Punkte im Local Storage auf 0 setzen
            document.getElementById("punkte").textContent = 0; // Aktualisiere die Punkteanzeige
        }

        });

        document.getElementById('neinButton').addEventListener('click', function() {
            alert('Kein Problem. Du schaffst es nächstes Mal!');
        });

        // Punkte aus dem Local Storage laden und anzeigen
        const gespeichertePunkte = parseInt(localStorage.getItem("punkte")) || 0;
        document.getElementById("punkte").textContent = gespeichertePunkte;
    </script>
</body>
</html>





