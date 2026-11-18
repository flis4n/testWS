# Workshop: Manuell testning av Sauce Demo

Testobjekt: https://www.saucedemo.com/

**Syfte:** skriv spårbara testfall, byt testfall med ett annat par, utför testning, rapportera avvikelser och spela in ett automatiserat test.

## Arbetsgång (2 timmar)

| Tid | Aktivitet | GitHub-arbete |
| --- | --- | --- |
| 10:00–10:10 | Introduktion | Öppna ett repository från template |
| 10:10–10:45 | Del A: skriv testfall | Redigera `testfall.md`, skapa commit |
| 11:00–11:05 | Byte | Skicka länken till en testare |
| 11:05–11:35 | Del B: kör testerna | Fyll i `testkorning.md`, skapa Issues för avvikelser |
| 11:15–11:30 | Del C: återkoppling | Kommentera testresultaten; förbättra testfall |
| 11:30–12:00 | Del D: automatisera | Spela in `TC-LOG-01`; lägg en `.side`- eller Recorder-JSON-fil i `automation/` |
| 12:00 | Avslut |

**Testkonton** (endast för Sauce Demos öppna demo): `standard_user` och `locked_out_user`. Lösenord: `secret_sauce`. Publicera aldrig verkliga lösenord eller personuppgifter i detta repository.

## Byte mellan testare

1. Den som **skrev** testfallen delar repo-länken med en annan.
2. Det **testande** paret följer teststegen utan muntliga förklaringar och dokumenterar sitt resultat i `testkorning.md`.
3. Verkliga avvikelser från kraven rapporteras som GitHub **Issues** i repositoryt. Välj mallen `Buggrapport`.
4. Oklarheter i testfall noteras som feedback, inte automatiskt som buggar i systemet.
5. Den som skrev testfallen gör förbättringar och länkar till commit eller pull request.


## Definition av klart

- Minst 12 testfall, inklusive minst 4 negativa och 2 gränsvärdestester.
- Alla 13 krav (`LOG-01` till `LOG-07`, `CRT-01` till `CRT-06`) täcks av minst ett testfall; ett testfall kan täcka flera krav.
- Testresultaten är reproducerbara och hänvisar till relevanta testfalls-ID:n.
- Buggar har steg, förväntat/faktiskt resultat och allvarlighetsgrad.
- Minst ett automatiserat test innehåller en **kontroll** av förväntat resultat, inte bara klicksekvens.
- Avsluta med: *Kan systemet släppas? På vilka grunder?*

Läs `automation/README.md` innan automatiseringen. Selenium IDE finns numera som separat program, inte som officiellt Chrome-tillägg. Chrome DevTools Recorder är installationsfritt alternativ.
