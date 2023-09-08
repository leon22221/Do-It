<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Frage</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button onclick="window.location.href='https://leon22221.github.io/Site-L/'">Ja</button>
    <button id="neinButton">Nein</button>
    <a href="https://leon22221.github.io/Site-L/">SiteL</a>

    <script>
       // JavaScript-Code zur Interaktion mit den Buttons
        document.getElementById('jaButton').addEventListener('click', function() {
            <a href="https://leon22221.github.io/Site-L/">testz</a>
            // JavaScript-Code, um Punkte zu vergeben und zu speichern
        let punkte = 0;

        document.getElementById("jaButton").addEventListener("click", function() {
            punkte += 10;
            document.getElementById("punkte").textContent = punkte;

            // Punkte in den Local Storage speichern
            localStorage.setItem("punkte", punkte);
        });

            // Aktualisiere die Anzeige der Punkte auf der Seite
            document.getElementById('punkte').textContent = aktuellePunkte;
        }

        });

        document.getElementById('neinButton').addEventListener('click', function() {
            alert('Kein Problem. Du schaffst es nächstes Mal!');
        });
    </script>
</body>
</html>
