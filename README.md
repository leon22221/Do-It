
<!DOCTYPE html>
<html>
<head>
    <title>Frage: Hast du die Aufgabe erledigt?</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button id="jaButton">Ja</button>
    <button id="neinButton">Nein</button>

    <script>
        // JavaScript-Code, um auf Klicks der Schaltflächen zu reagieren
        document.getElementById("jaButton").addEventListener("click", function() {
            alert("Gut gemacht! Die Aufgabe ist erledigt.");
        });

        document.getElementById("neinButton").addEventListener("click", function() {
            alert("Kein Problem. Du kannst die Aufgabe später erledigen.");
        });
    </script>
</body>
</html>
