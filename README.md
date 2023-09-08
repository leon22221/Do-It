<html>
<head>
    <title>Frage</title>
</head>
<body>
    <h1>Hast du die Aufgabe erledigt?</h1>
    
    <form>
        <input type="button" value="Ja" onclick="antwort('Ja');">
        <input type="button" value="Nein" onclick="antwort('Nein');">
    </form>
    
    <p id="ergebnis"></p>

    <script type="text/javascript">
        function antwort(antwort) {
            var applet = document.getElementById("java-applet");
            applet.antwort(antwort);
        }
    </script>

    <applet id="java-applet" code="InteraktivesApplet.class" width="0" height="0">
        <param name="java_arguments" value="-Xmx128M">
    </applet>
</body>
</html>
