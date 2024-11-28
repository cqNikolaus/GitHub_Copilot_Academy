![Comquent Academy](./images/comquent-academy-logo.png?raw=true "Comquent Academy")
# GitHub Copilot Workshop - Übungen
### Übung 1 - Gute Prompts erstellen
#### In dieser Übung lernen wir, wie Copilot anhand der von uns bereitgestellten Informationen Code generiert.
1. Erstelle eine neue Datei. Wir nutzen für dieses Beispiel eine JavaScript-Datei. Erstelle sie über das Interface oder gib Folgendes in deinem Terminal ein:

   ```bash 
   code index.js
   ```

   Anschließend sollte die Datei in deinem Editor geöffnet sein.

2. Sehen wir uns nun an, wie Copilot auf eine sehr generische Anfrage reagiert. Wir kommunizieren dabei über Kommentare. Gib in deiner `index.js` folgenden Kommentar ein:

   ```javascript
   // function to parse data
   ```

3. Wenn du jetzt Enter drückst, sollte Copilot direkt Code für die nächste Zeile vorschlagen. Durch Drücken von `Tab` kannst du diese Zeile akzeptieren, woraufhin direkt der nächste Vorschlag erscheint. Falls nicht, drücke zunächst erneut `Enter`, um in die nächste Zeile zu springen. So kannst du weitermachen, bis die Funktion vollständig ist.

   ![Kommentare nutzen](./images/copilot_03_ue1.png?raw=true "Kommentare nutzen")
  
4. In manchen Fällen kann es vorkommen, dass auch nach mehreren Sekunden kein Vorschlag angezeigt wird. Dann kann Copilot durch Eingeben des ersten zu erwartenden Buchstabens (in unserem Fall ein `f` für "function") ein kleiner "Schubser" gegeben werden, und der Vorschlag für den nächsten Teil des Codes sollte erscheinen.
    
Ein ähnliches Problem kann sich übrigens ergeben, wenn wir die Anfrage auf Deutsch formulieren:

   ```javascript 
   // Funktion zum Parsen von Daten
   ```

Hier ist es noch ein wenig wahrscheinlicher, dass Copilot nicht auf Anhieb einen sinnvollen Vorschlag macht, sondern möglicherweise sogar selbst einen weiteren Kommentar hinzufügen möchte. Auch hier hilft das "Anstupsen" durch Eingabe des ersten Buchstabens, den wir sehen wollen: `f`.

5. Unser Prompt per Kommentar ist in jedem Fall noch nicht spezifisch genug, damit Copilot weiß, was wir tun möchten. Entferne den Code und versuche es mit:
   ```javascript
   // function to parse url
   ```

6. Drücke `Enter` und du wirst vermutlich eine Zeile wie diese sehen:
   ```javascript
   function parseURL(url) {
   ```
7. Drücke `Tab`, um den Vorschlag anzunehmen, und wieder `Enter`. So kannst du dir Stück für Stück deine Funktion "zusammenbauen" lassen. Wie zuvor gilt: Sollte kein (brauchbarer) Vorschlag kommen, hilft das "Anstupsen" durch Eingabe eines Buchstabens (oft auch schon durch Tasten wie `Leertaste`, `Backspace` oder `Enter`).  

8. Wirklich zufrieden wirst du mit dem Ergebnis wohl nicht sein. Copilot kann auch alternative Vorschläge anzeigen. Lösche dazu alles bis auf die erste Zeile der Funktion und platziere den Cursor am Ende der Zeile.

9. Drücke `Strg + Enter`. Es öffnet sich ein Fenster mit weiteren Vorschlägen. Unter Umständen kann das Generieren dieser Vorschläge ein paar Sekunden dauern. Diese werden in ihrer Vollständigkeit und Qualität mitunter stark variieren. Gefällt dir einer, klicke auf "Accept suggestion", um den Code zu übernehmen.

    ![Alternative Vorschlaege](./images/copilot_04_ue1.png?raw=true "Alternative Vorschlaege")

10. Lass uns jetzt noch einmal versuchen, eine noch spezifischere Anfrage zu stellen. Lösche deinen gesamten Code, und gib anstelle eines Kommentars einen Funktionsnamen ein. Drücke noch nicht `Enter` oder `Tab`:
   
    ```javascript
    function splitURLandReturnComponents
    ```
11. Mit diesem Namen sollte Copilot eine vollständige Funktion vorschlagen - tatsächlich sogar mehrere. Bewege die Maus über den Code und ein kleines Fenster sollte erscheinen. Hier siehst du, wie viele Optionen zur Auswahl stehen. Klicke auf ">" bzw. "<", um die Optionen durchzuschalten, und auf "Akzeptieren" (`Tab`), um den jeweiligen Vorschlag in deinen Code zu übernehmen.

    ![Optionen durchschalten](./images/copilot_05_ue1.png?raw=true "Optionen durchschalten")

<br>

---

<br>

### Übung 2 - Code vereinfachen
#### In dieser Übung sehen wir uns an, wie Copilot uns dabei helfen kann, bestehenden Code zu vereinfachen und übersichtlicher zu machen.

1. Erstelle eine neue Datei `primzahlen.py`, wie in Übung 1 per Interface oder Terminal:
   
   ```bash
   code primzahlen.py
   ```
   
2. Schreibe den Anfang einer Funktion:
   
   ```python
   def is_prime(n):
   ```
   
3. Platziere den Cursor am Ende der Zeile.
   
   ![Code Vereinfachung 01](./images/copilot_07_ue2.png?raw=true "Code Vereinfachung 01")
   
4. Drücke `Strg + Enter`, um die verfügbaren Vorschläge anzuzeigen.
   
5. Wenn möglich, wähle eine der Optionen aus, die dir komplexer erscheint oder länger als die anderen ist. Klicke anschließend auf "Accept suggestion".
   
   ![Komplexere Funktion](./images/copilot_08_ue2.png?raw=true "Komplexere Funktion")

6. Markiere jetzt deinen Code und öffne anschließend das Chat Fenster in der Seitenleiste rechts oder durch `Strg + Alt + I`.

7. Weise Copilot in deinen Worten an, den Code zu vereinfachen (früher mit `/simplify`). Je nachdem, wie viel Spielraum der Code für Optimierungen lässt, kannst du dabei auch spezifischer werden. **Hinweis:** In den meisten Fällen erhältst du eine Antwort in der Sprache, in der du die Anfrage formuliert hast. Beispiele könnten sein:
   
   - ```Vereinfache```
   
   - ```Vereinfache den Code```
   
   - ```Schreibe den Code klarer und besser verständlich```
   
   - ```Verbessere die Lesbarkeit und Effizienz dieser Funktion, ohne die Funktionalität zu ändern. Bevorzuge pythonische Lösungen.```

     
  
8. Fahre mit dem Mauszeiger über die Antwort und wähle "Im Editor anwenden" aus.
  
   ![Vereinfache Code](./images/copilot_09_ue2.png?raw=true "Vereinfache Code")

9. Anschließend kannst du die Änderung im Editor mit "Show Changes" anzeigen lassen, akzeptieren oder verwerfen.

   ![Änderungen anzeigen](./images/copilot_10_ue2.png?raw=true "Änderungen anzeigen")

    Experimentiere ruhig mit Anfragen in Programmiersprachen und Funktionen, die du gut kennst. So bekommst du ein besseres Gefühl dafür, wie Copilot Code vereinfachen kann.

10. (Optional) Copilot kann verschiedene KI-Modelle zur Verarbeitung deiner Anfragen nutzen, die sich in ihrer Qualität unterscheiden können. Wie sieht eine Vereinfachung mit dem aktuell leistungsfähigsten Modell "o1-preview" im Vergleich zu "GPT 4o" aus?  
    Beachte: "o1-preview" braucht teils deutlich länger, um eine Antwort zu generieren. 

   ![Modell wählen](./images/copilot_11_ue2.png?raw=true "Änderungen anzeigen")

11. Jetzt wollen wir uns ansehen, wie Copilot einen Fehler im Code korrigieren kann. Baue einen Fehler ein, indem du eine Variable in deiner Funktion durch eine andere ersetzt, die nicht existiert, z.B. "x" statt "n".

    ![Fehler einbauen](./images/copilot_12_ue2.png?raw=true "Fehler einbauen")

12. Markiere deinen Code. Es erscheint ein gelbes Glühbirnen- oder Sternsymbol in der Nähe des Codes. Klicke darauf, und du erhältst unter anderem die Optionen, den Code mit Copilot zu korrigieren oder dir den Fehler erklären zu lassen.
    
13. Klicke auf "Mit Copilot korrigieren"

14. Nach ein paar Sekunden sollte Copilot eine Korrektur vorschlagen und vermutlich eine Erklärung dazu liefern. Mit einem Klick auf "Annehmen" kannst du sie akzeptieren. Der kleine Pfeil rechts lässt dich die Änderungen anzeigen und umschalten.

    ![Mit Copilot korrigieren](./images/copilot_13_ue2.png?raw=true "Mit Copilot korrigieren")

**„Hinweis:** Wie du an deiner Anfrage im Chatfenster sehen kannst, wird automatisch das Slash-Kommando `/fix` genutzt. Dieser Befehl weist Copilot an, Fehler im Code zu finden und zu korrigieren, ohne dass ein ausführlicher Prompt erforderlich ist. Du kannst daher auch direkt `/fix` in den Copilot-Chat (`Strg + Alt + I`) oder Inline-Chat (`Strg + I`) schreiben. Alternativ sind selbstverständlich auch Anweisungen in freier Formulierung möglich. Bei umfangreichen oder komplexeren Fehlern kann es sinnvoller sein, eine detaillierte Anfrage mit zusätzlichem Kontext im Chat zu stellen.“

<br>

---

<br>

### Übung 3 - Code verstehen und kommentieren mit Copilot
#### In dieser Übung nutzen wir Copilot, um bestehenden Code zu analysieren, zu erklären und automatisch sinnvolle Dokumentationskommentare zu generieren.

1. Jetzt, wo wir etwas Code haben, mit dem wir arbeiten können, schauen wir uns an, was Copilot sonst noch für uns tun kann. Lass dir den aktuellen Code in deiner `primzahlen.py`-Datei erklären. Markiere den Code und öffne den Copilot-Inline-Chat mit der Tastenkombination `Cmd + I`.

2. Auch hier können wir, anstatt eine längere Anfrage zu stellen, eines der eingebauten Slash-Kommandos nutzen:  
   Gib `/explain` ein und drücke `Enter`.

   ![Code erklären lassen](./images/copilot_14_ue3.png?raw=true "Code erklären lassen")

3. Wenn dir die Antwort unklar oder unvollständig ist, kannst du weitere Fragen stellen, z.B.:

   ```plaintext
   Kannst du den Algorithmus genauer erklären?
   ```

**Hinweis:** Möchtest du die Erklärung in deiner Sprache haben, kannst du Copilot mit Formulierungen wie "/explain Antworte auf Deutsch" dazu anweisen. 
   
4. (Optional) Wir können uns den Code auch über Kommentare erklären lassen. Das ist eine ältere Methode; der Chat bietet mittlerweile mehr Möglichkeiten.
   Gib den folgenden Kommentar unterhalb deiner Funktion ein: 

   ```python
   # Erkläre den Code oben Zeile für Zeile
   ```

   Copilot sollte die Antwort nun in den Kommentaren anzeigen. Drücke `Tab`, um die Zeile zu akzeptieren und `Enter` um in die nächste Zeile zu springen und auf den nächsten Schritt der Erklärung zu warten.

   ![Code erklären lassen per Kommentar](./images/copilot_15_ue3.png?raw=true "Code erklären lassen per Kommentar")

   Mit dem Präfix `q:` lässt sich auch direkt eine Frage als Kommentar stellen. Die Antwort können wir, falls sie nicht automatisch erscheint, durch einen weiteren Kommentar, der mit `a:` beginnt, erzeugen lassen.

   ![Erklärung per Kommentar Präfix](./images/copilot_16_ue3.png?raw=true "Erklärung per Kommentar Präfix")

5. Nun wollen wir das doc-Feature ausprobieren, um automatisch Dokumentationskommentare zu erstellen. Markiere deine Funktion.
   
6. Drücke jetzt `Strg + I` für den Inline-Chat, gib das Slash-Kommando `/doc` ein und drücke `Enter`. Copilot sollte nun automatisch einen Docstring für deinen Code generieren. Klicke auf "Annehmen", um den Vorschlag zu akzeptieren.
   Zusätzlich kannst du Copilot auch hier in eigener Formulierung, z.B. die gewünschte Sprache oder die Ausführlichkeit der zu generierenden Kommentare, vorgeben.
   
   ![Doc-feature](./images/copilot_17_ue3.png?raw=true "Doc-feature")

<br>

---

<br>

### Übung 4 - Tests mit Copilot generieren
#### In dieser Übung werden wir mit Copilot automatische Tests für unsere Funktionen generieren. 

1. Wir wollen uns nun Unit-Tests für unsere Primzahlen-Funktion erstellen lassen. Schreibe dazu folgenden Kommentar unterhalb deiner Funktion:

   ```python
   # Erstelle eine Funktion, um 5 Unit-Tests für den obigen Code durchzuführen
   ```

2. Drücke `Enter` und warte ggf. einen Moment, bis Copilot eine Antwort generiert hat, und drücke dann `Tab`, um den Code anzunehmen. Falls du keinen Vorschlag erhältst, gib Copilot schon einmal den Funktionsnamen vor:

   ```python
   def test_is_prime():
   ```
   
  ![Tests generieren](./images/copilot_18_ue4.png?raw=true "Tests generieren")
  

3. Was, wenn wir gar nicht wissen, wie man den Code überhaupt testet? Fragen wir Copilot. Markiere den Code deiner Funktion.

  ![Prime-Funktion markieren](./images/copilot_19_ue4.png?raw=true "Prime-Funktion markieren")

4. Öffne den Copilot-Chat (`Strg + Alt + I`) und stelle Copilot eine Frage wie die folgende:

   ```
   Erkläre mir, wie ich diesen Code testen kann
   ```

   **Hinweis:** Sollte Copilot dich auffordern, dein Testframework zu bestätigen, klicke auf "Akzeptieren" und stelle die Anfrage erneut.



5. Wie du in der Antwort siehst, hat Copilot vermutlich automatisch das Kommando `/test` genutzt und eine Erklärung hinzugefügt. Klicke auf den Haken, um den Vorschlag zu übernehmen, und lasse Copilot, wie in der Erklärung beschrieben, automatisch eine neue Datei erstellen. Diese muss dann noch unter dem beschriebenen Namen ("test_primzahlen.py") gespeichert werden.  

![Test erklären](./images/copilot_20_ue4.png?raw=true "Test erklären")

<br>

---

<br>

### Übung 5 – SQL-Abfragen mit Copilot erstellen
#### In dieser Übung entdecken wir anhand von Beispielen, wie Copilot beim Schreiben von SQL-Abfragen behilflich sein kann.

1. Erstelle eine neue Datei `dev.sql`.
   
Anschließend sollte diese Datei in einem Tab im Editor geöffnet sein. Stell dir vor, wir möchten mit einer Datenbank arbeiten, die Datensätze für Studierende, Mitarbeitende, Lehrpläne, Kurse, Fakultäten, Standorte und Einschreibungen eines Universitätssystems enthält. Schauen wir doch mal, was Copilot für eine Abfrage generieren würde, um alle Studierenden in einem Kurs zu erhalten – und das ohne jeglichen zusätzlichen Kontext.

2. Gib den folgenden Kommentar im Chat oder Inline-Chat ein und akzeptiere den erhaltenen Vorschlag:

   ```plaintext
   Definiere eine SELECT-Abfrage, um alle Studierenden in einem Kurs zu erhalten
   ```

3. Jetzt wollen wir uns ansehen, ob wir andere Ergebnisse bekommen, wenn wir Copilot zusätzlichen Kontext bereitstellen. In unserem GitHub-Repository befindet sich eine Datei `create-tables.sql`, die eine Reihe von Tabellen enthält. Wenn du möchtest, kannst du sie dir ansehen oder in einem neuen Tab öffnen, für unser Beispiel spielt das aber keine Rolle.

4. Um nun explizit die Datei `create-tables.sql` dem Kontext hinzuzufügen, stelle sicher, dass du deine `dev.sql` im aktiven Tab geöffnet hast. Öffne dann das Chatfenster und ziehe die Datei `create-tables.sql` aus dem Explorer auf der linken Seite per Drag and Drop in das Chatfenster. Im Eingabefenster deines Copilot-Chats solltest du nun beide Dateinamen sehen. Gib deine Anfrage aus Schritt 2 erneut ein und du wirst feststellen, dass Copilot nun die Abfrage mit Bezug auf die Tabellen aus `create-tables.sql` erstellt.

   **Hinweis:** Anstatt die Datei per Drag and Drop hinzuzufügen, kannst du auch im Chat die Variable `#file` nutzen, um `create-tables.sql` auszuwählen.

![SQL Abfrage mit Copilot](./images/copilot_21_ue5.png?raw=true "SQL Abfrage mit Copilot")

5. Möglicherweise wollen wir auch einen Index verwenden, um die Abfragen zu beschleunigen. Öffne wieder den Chat oder Inline-Chat und bitte Copilot um Folgendes:

   ```plaintext
   Erstelle einen Index, um die Performance der Abfrage zu verbessern
   ```
   ![Index erstellen](./images/copilot_22_ue5.png?raw=true "Index erstellen")

6. Angenommen, wir möchten zusätzlich eine Tabelle erstellen, um die Anwesenheit von Studierenden zu erfassen. Wir können Copilot bitten, die Tabellen-Definition für uns zu erstellen:

   ```plaintext
   Definiere eine Tabelle für die Anwesenheit von Studierenden, um die Anwesenheit nach Klassen zu erfassen
   ```

   ![Tabelle erstellen](./images/copilot_23_ue5.png?raw=true "Tabelle erstellen")

7. Copilot kann auch Stored Procedures erstellen. Versuche es mal mit folgendem Prompt:

   ```plaintext
   Generiere eine Stored Procedure, um Kursanmeldungen nach Standort abzurufen
   ```
    
   oder auch direkt mit einer komplexeren Anfrage:

   ```plaintext
   Erstelle eine Stored Procedure, um Details zu Instruktoren zu erhalten, die mit einem Standort verbunden sind. Schließe Instruktor-Details, Standort-Details und Kurse ein, die dem Instruktor zugeordnet sind. Verwende instructor_id als Eingabeparameter
   ```

   ![Stored Procedure](./images/copilot_24_ue5.png?raw=true "Stored Procedure")

<br>

---

<br>

### Copilot und die Aktualität von Daten
#### In dieser Übung werden werden wir herausfinden, was es für Möglichkeiten gibt, wenn Copilot nicht die aktuellsten Informationen hat.

1. Erstelle wie in den Übungen zuvor eine neue Datei und nenne sie diesmal `explore.go`.

2. Nun wollen wir einen Generator für Zufallszahlen in Go erstellen. Weise Copilot im Inline-Chat (`Strg + I`) an:

   ```go
   Schreibe eine Funktion für einen Zufallszahlengenerator
   ```
   ![Zufallszahlen](./images/copilot_26_ue6.png?raw=true "Zufallszahlen")
   
3. Copilot hat vermutlich die rand.Seed Funktion genutzt. Diese Funktion ist seit Go 1.20 allerdings [veraltet](https://cs.opensource.google/go/go/+/refs/tags/go1.21.0:src/math/rand/rand.go;l=394)

4. Fragen wir doch einmal Copilot ob das stimmt:

   ```plaintext
   Ist die rand.Seed Funktion in Go veraltet?
   ```
   ![Seed in Go](./images/copilot_25_ue6.png?raw=true "Seed in Go")

5. Um Copilots Wissenslücken für den Moment zu schließen, gibt es nun mehrere Möglichkeiten. Eine davon ist, aktuelle Codeausschnitte als Informationen bereitzustellen. Lösche den Inhalt deiner `explore.go` und füge stattdessen folgenden Ausschnitt aus der [Go-Dokumentation](https://pkg.go.dev/math/rand) als Kommentar ein:

   ```go
   // Create and seed the generator.
	// Typically a non-fixed seed should be used, such as time.Now().UnixNano().
	// Using a fixed seed will produce the same output on every run.
	// r := rand.New(rand.NewSource(99))
   ```

6. Stelle deine Anfrage aus Schritt 2 nun unterhalb der eingefügten Zeilen erneut.

   ![Zufallszahlen mit Kontext Doc](./images/copilot_27_ue6.png?raw=true "Zufallszahlen mit Kontext Doc")

   Copilot sollte automatisch die neue Funktion aus der Dokumentation nutzen.  
   **Hinweis:** Du kannst diese zusätzlichen Informationen natürlich auch direkt zu deiner Anfrage im Chat bereitstellen, anstatt sie als Kommentar hinzuzufügen.

7. Eine andere Möglichkeit, die uns seit Ende 2024 zur Verfügung steht, ist Copilot die aktuellen Informationen selbstständig online suchen zu lassen. Voraussetzung dafür ist, dass zuvor in den GitHub Copilot Einstellungen (https://github.com/settings/copilot) die Option "Copilot access to Bing" aktiviert wurde.

   ![Copilot access to Bing](./images/copilot_28_ue6.png?raw=true "Copilot access to Bing")

8. Ist dieses Feature aktiviert, können wir im Copilot Chat mit `@github` auf die GitHub-spezifischen Features zugreifen und Copilot mit `#web` mitteilen, dass die Onlinesuche für die Anfrage eingesetzt werden soll.
   Die gesamte Anfrage könnte dann also z.B. so aussehen:

   ```plaintext
   @github #web Ist die rand.Seed Funktion in Go veraltet?
   ```
   
   ![Copilot Websuche](./images/copilot_29_ue6.png?raw=true "Copilot Websuche")

   **Hinweis:** Zum aktuellen Zeitpunkt funktioniert das Feature möglicherweise noch nicht in den Codespaces. Wundere dich also nicht, falls du eine Fehlermeldung erhältst. In deiner IDE sollte es klappen.

   
   
   

