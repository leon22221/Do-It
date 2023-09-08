<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fragene</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    <button id="jaButton" onclick="window.location.href = 'https://leon22221.github.io/Site-L/';">Ja</button>
    <button id="neinButton" onclick="window.location.href = 'https://leon22221.github.io/Site-L/';">Nein</button>

 <script>
        // JavaScript-Code zur Interaktion mit den Buttons
document.getElementById('jaButton').addEventListener('click', function() {
    // JavaScript-Code, um Gesamtpunkte zu vergeben und zu speichern
    let gesamtpunkte = parseInt(localStorage.getItem("punkte")) || 0; // Gesamtpunkte aus dem Local Storage laden oder auf 0 setzen
    punkte += 10;
    localStorage.setItem("punkte", punkte); // Gesamtpunkte in den Local Storage speichern
    document.getElementById("punkte").textContent = punkte; // Aktualisiere die Gesamtpunkte-Anzeige

    // JavaScript-Code, um Punktzahl der erledigten Aufgaben zu vergeben und zu speichern
    let ErlAuf = parseInt(localStorage.getItem("ErlAuf")) || 0; // Punktzahl der erledigten Aufgaben aus dem Local Storage laden oder auf 0 setzen
    ErlAuf += 1;
    localStorage.setItem("ErlAuf", ErlAuf); // Punktzahl der erledigten Aufgaben in den Local Storage speichern
    document.getElementById("ErlAuf").textContent = ErlAuf; // Aktualisiere die Punktzahl der erledigten Aufgaben-Anzeige
});

        document.getElementById('neinButton').addEventListener('click', function() {
                    alert('Kinda Goofy von dir, guck dir deine Werte an!');
        });
    </script>
</body>
</html>





