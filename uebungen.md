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
    Beachte: "o1-preview" braucht teils deutlich länger um eine Antwort zu generieren. 

   ![Modell wählen](./images/copilot_11_ue2.png?raw=true "Änderungen anzeigen")

11. Jetzt wollen wir uns ansehen, wie Copilot einen Fehler im Code korrigieren kann. Baue einen Fehler ein, indem du eine Variable in deiner Funktion durch eine andere ersetzt, die nicht existiert, z.B. "x" statt "n".

    ![Fehler einbauen](./images/copilot_12_ue2.png?raw=true "Fehler einbauen")

12. Markiere deinen Code. Es erscheint ein gelbes Glühbirnen- oder Sternsymbol in der Nähe des Codes. Klicke darauf, und du erhältst unter anderem die Optionen, den Code mit Copilot zu korrigieren oder dir den Fehler erklären zu lassen.
    
13. Klicke auf "Mit Copilot korrigieren"

14. Nach ein paar Sekunden sollte Copilot eine Korrektur vorschlagen und vermutlich eine Erklärung dazu liefern. Mit einem Klick auf "Annehmen" kannst du sie akzeptieren. Der kleine Pfeil rechts lässt dich die Änderungen anzeigen und umschalten.

    ![Mit Copilot korrigieren](./images/copilot_13_ue2.png?raw=true "Mit Copilot korrigieren")

    **„Hinweis:** Wie du an deiner Anfrage im Chatfenster sehen kannst, wird automatisch das Slash-Kommando `/fix` genutzt. Dieser Befehl weist Copilot an, Fehler im Code zu finden und zu korrigieren, ohne dass ein ausführlicher Prompt erforderlich ist. Du kannst daher auch direkt `/fix` in den Copilot-Chat (`Strg + Alt + I`) oder Inline-Chat (`Strg + I`) schreiben. Alternativ sind selbstverständlich auch Anweisungen in freier Formulierung möglich. Bei umfangreichen oder komplexeren Fehlern kann es sogar sinnvoller sein, eine detaillierte Anfrage mit zusätzlichem Kontext im Chat zu stellen.“

<br>

---

<br>

### Übung 3 - Code verstehen und kommentieren mit Copilot
#### In dieser Übung nutzen wir Copilot, um bestehenden Code zu analysieren, zu erklären und automatisch sinnvolle Kommentare zu generieren.

1. Jetzt, wo wir etwas Code haben, mit dem wir arbeiten können, schauen wir uns an, was Copilot sonst noch für uns tun kann. Lass dir den aktuellen Code in unserer `primzahlen.py`-Datei erklären. Markiere den Code und öffne den Copilot-Inline-Chat mit der Tastenkombination `Cmd + I`.

2. Auch hier können wir, anstatt eine längere Anfrage zu stellen, eines der eingebauten Slash-Kommandos nutzen:  
   Gib `/explain` ein und drücke `Enter`.

   ![Code erklären lassen](./images/copilot_14_ue3.png?raw=true "Code erklären lassen")

4. Wenn dir die Antwort unklar oder unvollständig ist, kannst du weitere Fragen stellen, z.B.:

   ```plaintext
   Kannst du den Algorithmus genauer erklären?
   ```

   **Hinweis:** Möchtest du die Erklärung in deiner Sprache haben, kannst du Copilot mit Formulierungen wie "/explain Antworte auf Deutsch" dazu anweisen. 
   
5. (Optional) Wir können uns den Code auch über Kommentare erklären lassen. Das ist eine ältere Methode; der Chat bietet mittlerweile mehr Möglichkeiten.
   Gib den folgenden Kommentar unterhalb deiner Funktion ein: 

   ```python
   # Erkläre den Code oben Zeile für Zeile
   ```
   Copilot sollte die Antwort nun in den Kommentaren anzeigen. Drücke `Tab`, um die Zeile zu akzeptieren und `Enter` um in die nächste Zeile zu springen und auf den nächsten Schritt der Erklärung zu warten.

   ![Code erklären lassen per Kommentar](./images/copilot_15_ue3.png?raw=true "Code erklären lassen per Kommentar")

   Mit dem Präfix `q:` lässt sich auch direkt eine Frage als Kommentar stellen. Die Antwort können wir, falls sie nicht automatisch erscheint, durch einen weiteren Kommentar, der mit `a:` beginnt, erzeugen lassen.

   ![Erklärung per Kommentar Präfix](./images/copilot_16_ue3.png?raw=true "Erklärung per Kommentar Präfix")

6. Nun wollen wir das doc-Feature ausprobieren, um automatisch Dokumentationskommentare zu erstellen. Markiere deine Funktion.
   
7. Drücke jetzt `Strg + I` für den Inline-Chat, gib das Slash-Kommando `/doc` ein und drücke `Enter`. Copilot sollte nun automatisch einen Docstring für deinen Code generieren. Klicke auf "Annehmen", um den Vorschlag zu akzeptieren.
   Zusätzlich kannst du Copilot auch hier in eigener Formulierung, z.B. die gewünschte Sprache oder die Ausführlichkeit der zu generierenden Kommentare, vorgeben.
   
   ![Doc-feature](./images/copilot_17_ue3.png?raw=true "Doc-feature")
   

   
   
   
  
   
