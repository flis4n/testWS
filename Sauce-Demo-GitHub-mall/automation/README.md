# Automatisering av TC-LOG-01

## A. Selenium IDE som separat program

1. Hämta version för ditt operativsystem från https://github.com/SeleniumHQ/selenium-ide/releases. Den tidigare officiella Chrome-extensionen finns inte längre i Chrome Web Store.
2. Starta Selenium IDE. Skapa nytt projekt, exempelvis `SauceDemo-par-03`. Ange bas-URL `https://www.saucedemo.com/`.
3. Spela in ett nytt test med namn `TC-LOG-01`: öppna Sauce Demo, ange `standard_user`, ange `secret_sauce`, klicka `Login`.
4. Stoppa inspelningen.
5. Lägg till en verifiering, om kommandoredigeraren finns i er version: `assert text`, target `css=[data-test="title"]`, value `Products`. På vissa versioner kan uppspelning/editorn skilja sig; be läraren om hjälp.
6. Kör testet från utloggat läge. Testet ska bli godkänt.
7. Ändra det inspelade lösenordet till ett felaktigt värde och kör om. Testet ska då bli underkänt eftersom `Products` inte visas. Om er version inte låter er ändra steg, spela in ett andra test med fel lösenord och samma verifiering.
8. Spara projektet (normalt `.side`) i denna mapp och gör en commit.

**OBS!** De nya desktop-versionerna är fortfarande beta och installationsfilerna kan vara osignerade. Installera endast enligt skolans IT-policy och gör ett funktionstest före lektionen. Använd endast demokonton.

## B. Chrome DevTools Recorder – inget tillägg och ingen installation

1. Öppna Sauce Demo i Chrome; logga ut vid behov.
2. Tryck `F12` (alternativt högerklick → `Inspect`) för att öppna DevTools.
3. Tryck `Ctrl+Shift+P` (`Cmd+Shift+P` på Mac), skriv `Show Recorder panel`, tryck Enter.
4. Välj `Create a new recording`, ge namnet `TC-LOG-01`, klicka `Start recording`.
5. Utför inloggning med `standard_user` och `secret_sauce`.
6. I Recorder: välj `Add assertion` och välj elementet som visar `Products`. Kontrollera att exempelvis egenskapen `innerText` är `Products` (i Recorder som property `.innerText`).
7. Stoppa inspelning och tryck `Replay`. Kontrollera att uppspelningen går igenom.
8. Ändra inmatningssteget för lösenordet till `fel_losen`, kör `Replay` igen och förvänta dig att assertionen misslyckas.
9. Exportera inspelningen till JSON från Recorder och lägg filen i `automation/`; gör commit.

Dokumentation: https://developer.chrome.com/docs/devtools/recorder/overview och https://developer.chrome.com/docs/devtools/recorder/reference

**Bedömning:** enbart inspelade klick räcker inte. Testet ska verifiera en förväntad effekt (t.ex. rubriken `Products`).
