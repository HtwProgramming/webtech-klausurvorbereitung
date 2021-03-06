# Chuck Norris App

## Aufgaben

Sie werden im Rahmen dieser Aufgabe eine simple Webanwendung implementieren, die dem User zufällige Chuck Norris Sprüche anzeigt.

1. Forken und Clonen Sie das Repository und starten Sie die Spring Boot Anwendung. Sie benötigen Gradle 7 und idealerweise Java 16.

2. Rufen Sie die Startseite der Anwendung auf. Navigieren Sie dazu in Ihrem Browser zur Adresse `http://localhost:8080`.
Ihnen sollte die folgende Seite angezeigt werden:
   
<img width="894" alt="webpage" src="https://user-images.githubusercontent.com/81008192/124390313-3fc17380-dceb-11eb-9a7d-9d17308c7a7e.png">

3. Implementieren Sie das Interface `QuotesService`. Die Implementierungsdetails entnehmen Sie bitte dem JavaDoc.

4. Implementieren Sie einen Rest-Controller, deren Endpunkt Sie anschließend aus einer Vue-Komponente aufrufen, um einen zufälligen Chuck Norris Spruch zu laden. Berücksichtigen Sie folgende Details:

    - der Controller soll die Implementierung des Interfaces `QuotesService` benutzen, um sich einen Chuck Norris Spruch zu holen
    - der Endpunkt soll unter `/rest/quote` und via `GET` erreichbar sein
    - der Client übermittelt den Index via Request-Parameter `index`, also z.B. `/rest/quote?index=53`
    - Verwenden Sie für die Rückgabe die Klasse `QuoteResponse` (ggf. mit `ResponseEntity` als Wrapper)
    - der Endpunkt soll dem Client ein JSON liefern

5. Es existiert in der Datei `resources/static/js/quotes.js` bereits eine Vue-Komponente, die aktuell jedoch keine Dynamik aufweist. Implementieren Sie die Methode `loadRandomQuote()`. Rufen Sie in der Methode Ihren Rest-Endpunkt auf. Verwenden Sie die Methode `getRandomInt()`, um Zufallszahlen zu erzeugen. Die Obergrenze sollte 80 sein. Sobald die Seite neu geladen wird, soll ein neuer Spruch geladen und angezeigt werden.

6. Erweitern Sie die Vue-Komponente wie folgt: Sobald der User auf Chuck Norris klickt, soll ein neuer Spruch angezeigt werden.
