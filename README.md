# Workshop: Manuell testning av Sauce Demo

Testobjekt: https://www.saucedemo.com/

**Syfte:** skriv spårbara testfall, byt testfall med ett annat par, utför testning, rapportera avvikelser och spela in ett automatiserat test.

## Arbetsgång (2 timmar)

| Tid | Aktivitet | GitHub-arbete |
| --- | --- | --- |
| 10:00–10:10 | Introduktion | Öppna ett eget repository från template |
| 10:10–11:00 | Del A: skriv testfall | Redigera `testfall.md`, skapa commit |
| 11:00–11:15 | PAUS |
| 11:15–11:20 | Byte | Byt testfall med en annan |
| 11:20–11:45 | Del B: kör testerna | Fyll i `testkorning.md`, skapa Issues för avvikelser |
| 11:45–12:00 | Del C: återkoppling | Kommentera testresultaten; förbättra testfall |
| 12:00 | Avslut |

**Testkonton** (endast för Sauce Demos öppna demo): `standard_user` och `locked_out_user`. Lösenord: `secret_sauce`. Publicera aldrig verkliga lösenord eller personuppgifter i detta repository.

## Byte mellan testare

1. Den som **skrev** testfallen delar repo-länken med en annan.
2. Det **testande** paret följer teststegen utan muntliga förklaringar och dokumenterar sitt resultat i `testkorning.md`.
3. Verkliga avvikelser från kraven rapporteras som GitHub **Issues** i repositoryt. Välj mallen `Buggrapport`.
4. Oklarheter i testfall noteras som feedback, inte automatiskt som buggar i systemet.
5. Den som skrev testfallen gör förbättringar och länkar till commit eller pull request.


## Definition av klart

- Minst 10 testfall, inklusive minst 2 negativa och 2 gränsvärdestester.
- Alla krav (`LOG-01` till `LOG-07`, `CRT-01` till `CRT-06`) täcks av minst ett testfall; ett testfall kan täcka flera krav.
- Testresultaten är reproducerbara och hänvisar till relevanta testfalls-ID:n.
- Buggar har steg, förväntat/faktiskt resultat och allvarlighetsgrad.
- Minst ett automatiserat test innehåller en **kontroll** av förväntat resultat, inte bara klicksekvens.
- Avsluta med: *Kan systemet släppas? På vilka grunder?*

## Frivillig bonusuppgift
Läs `automation/README.md` innan automatiseringen. Selenium IDE finns numera som separat program, inte som officiellt Chrome-tillägg. Chrome DevTools Recorder är installationsfritt alternativ.
Del D: automatisera | Spela in `TC-LOG-01`; lägg en `.side`- eller Recorder-JSON-fil i `automation/`
