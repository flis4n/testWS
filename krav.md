# Kravspecifikation (sammanfattning från workshopunderlaget)

## Inloggning (LOG)
- **LOG-01** Giltiga inloggningsuppgifter ger åtkomst till produktsidan.
- **LOG-02** Fel lösenord eller okänt användarnamn avvisas med felmeddelande; användaren stannar på inloggningssidan.
- **LOG-03** Tomt användarnamn ger felmeddelande.
- **LOG-04** Tomt lösenord ger felmeddelande.
- **LOG-05** Spärrad användare nekas inloggning med relevant felmeddelande.
- **LOG-06** Ej inloggad användare ska inte nå produktsidan med direktadress.
- **LOG-07** En inloggad användare kan logga ut och ska därefter inte nå skyddade sidor.

## Varukorg (CRT)
- **CRT-01** Produkt kan läggas till från produktlista och produktsida; knapp blir `Remove`.
- **CRT-02** Varukorgens ikon visar antal produkter; inget antal när den är tom.
- **CRT-03** Varukorgssidan visar korrekt namn, pris och antal för alla tillagda produkter.
- **CRT-04** Produkter kan tas bort både från produktlista och varukorgssida.
- **CRT-05** Varukorgsinnehåll kvarstår vid navigering mellan sidor.
- **CRT-06** Från varukorgen går det att återgå till att fortsätta handla. Kassa ingår inte.

Kravtexten är en kortversion av lärarens dokument. Vid tolkningsskillnader gäller det utdelade workshopdokumentet. Dokumentera även otydliga krav.
