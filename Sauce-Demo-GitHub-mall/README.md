# Workshop: Manuell testning av Sauce Demo

Testobjekt: https://www.saucedemo.com/

**Syfte:** skriv spårbara testfall, byt testfall med ett annat par, utför testning, rapportera avvikelser och spela in ett automatiserat test.

## Arbetsgång (2 timmar)

| Tid | Aktivitet | GitHub-arbete |
| --- | --- | --- |
| 00:00–00:10 | Introduktion | Öppna parets repository, fördela roller |
| 00:10–00:40 | Del A: skriv testfall | Redigera `testfall.md`, skapa commit |
| 00:40–00:45 | Byte | Skicka länken till ett annat par |
| 00:45–01:15 | Del B: kör testerna | Fyll i `testkorning.md`, skapa Issues för avvikelser |
| 01:15–01:30 | Del C: återkoppling | Kommentera testresultaten; författarna förbättrar minst två testfall |
| 01:30–01:55 | Del D: automatisera | Spela in `TC-LOG-01`; lägg en `.side`- eller Recorder-JSON-fil i `automation/` |
| 01:55–02:00 | Avslut | Skriv en kort släpprekommendation |

**Testkonton** (endast för Sauce Demos öppna demo): `standard_user` och `locked_out_user`. Lösenord: `secret_sauce`. Publicera aldrig verkliga lösenord eller personuppgifter i detta repository.

## Byte mellan par

1. Paret som **skrev** testfallen delar repo-länken med ett annat par.
2. Det **testande** paret följer teststegen utan muntliga förklaringar och dokumenterar sitt resultat i `testkorning.md` (eller ett delat dokument om ni saknar skrivrättigheter).
3. Verkliga avvikelser från kraven rapporteras som GitHub **Issues** i parets repository. Välj mallen `Buggrapport`.
4. Oklarheter i testfall noteras som feedback, inte automatiskt som buggar i systemet.
5. Paret som skrev testfallen gör två förbättringar och länkar till commit eller pull request.

Om repo är privat: ge det testande paret läs-/skrivbehörighet i förväg eller använd en gemensam kursorganisation. Om repo är offentligt: inga personuppgifter eller kurshemligheter.

## Definition av klart

- Minst 12 testfall, inklusive minst 4 negativa och 2 gränsvärdestester.
- Alla 13 krav (`LOG-01` till `LOG-07`, `CRT-01` till `CRT-06`) täcks av minst ett testfall; ett testfall kan täcka flera krav.
- Testresultaten är reproducerbara och hänvisar till relevanta testfalls-ID:n.
- Buggar har steg, förväntat/faktiskt resultat och allvarlighetsgrad.
- Minst ett automatiserat test innehåller en **kontroll** av förväntat resultat, inte bara klicksekvens.
- Avsluta med: *Kan systemet släppas? På vilka grunder?*

Läs `automation/README.md` innan automatiseringen. Selenium IDE finns numera som separat program, inte som officiellt Chrome-tillägg. Chrome DevTools Recorder är installationsfritt alternativ.
