<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Frage</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button id="jaButton">Ja</button>
    <button id="neinButton">Nein</button>

    <script>
        // JavaScript-Code zur Interaktion mit den Buttons
        document.getElementById('jaButton').addEventListener('click', function() {
            alert('Gut gemacht! Aufgabe erledigt.');
        });

        document.getElementById('neinButton').addEventListener('click', function() {
            alert('Kein Problem. Du schaffst es nächstes Mal!');
        });
    </script>
</body>
</html>





