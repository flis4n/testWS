# Testfall – fyll i och komplettera

**Instruktion:** skapa minst sju nya testfall så att ni får minst tolv totalt. Minst fyra negativa, två gränsvärdestester, samt täckning av alla LOG- och CRT-krav. Förkrav, data och observerbara resultat ska vara explicita. Ta inte bort exemplen nedan.

## TC-LOG-01 – Giltig inloggning
- **Krav:** LOG-01
- **Typ:** Positivt
- **Förkrav:** Användaren är utloggad. Ny ren session.
- **Testdata:** `standard_user` / `secret_sauce`
- **Steg:**
  1. Öppna `https://www.saucedemo.com/`.
  2. Skriv `standard_user` i fältet för användarnamn.
  3. Skriv `secret_sauce` i fältet för lösenord.
  4. Klicka på `Login`.
- **Förväntat resultat:** Produktsidan visas med rubriken `Products`.

## TC-LOG-02 – Fel lösenord
- **Krav:** LOG-02
- **Typ:** Negativt
- **Förkrav:** Utloggad, ny ren session.
- **Testdata:** `standard_user` / `fel_losen`
- **Steg:**
  1. Öppna `https://www.saucedemo.com/`.
  2. Skriv `standard_user` som användarnamn.
  3. Skriv `fel_losen` som lösenord.
  4. Klicka på `Login`.
- **Förväntat resultat:** Felmeddelande om att användarnamn och lösenord inte matchar visas; användaren stannar på inloggningssidan.

## TC-LOG-03 – Tomt användarnamn
- **Krav:** LOG-03
- **Typ:** Negativt
- **Förkrav:** Utloggad, ny ren session.
- **Testdata:** Tomt användarnamn / `secret_sauce`
- **Steg:**
  1. Öppna `https://www.saucedemo.com/`.
  2. Lämna användarnamnsfältet tomt.
  3. Skriv `secret_sauce` som lösenord.
  4. Klicka på `Login`.
- **Förväntat resultat:** Felmeddelande om att användarnamn krävs visas.

## TC-CRT-01 – Lägg till en produkt
- **Krav:** CRT-01, CRT-02
- **Typ:** Positivt
- **Förkrav:** Logga in som `standard_user`; varukorgen är tom.
- **Testdata:** `Sauce Labs Backpack`
- **Steg:**
  1. Öppna produktlistan.
  2. Klicka på `Add to cart` vid `Sauce Labs Backpack`.
- **Förväntat resultat:** Produktens knapp blir `Remove`; varukorgsikonen visar `1`.

## TC-CRT-02 – Ta bort enda produkten
- **Krav:** CRT-02, CRT-04
- **Typ:** Gränsvärde (1 → 0)
- **Förkrav:** Logga in som `standard_user`; varukorgen är tom.
- **Testdata:** `Sauce Labs Backpack`
- **Steg:**
  1. Klicka på `Add to cart` vid `Sauce Labs Backpack`.
  2. Klicka på `Remove` vid samma produkt.
- **Förväntat resultat:** Knappen blir `Add to cart`; ikonen visar inget antal.

---

## Mall att kopiera för varje nytt testfall

### TC-XXX-XX – [Titel]
- **Krav:** [LOG-XX / CRT-XX]
- **Typ:** [Positivt / Negativt / Gränsvärde]
- **Förkrav:** [Ren session, inloggning, varukorgens startläge]
- **Testdata:** [Exakta värden]
- **Steg:**
  1. [En handling]
  2. [En handling]
  3. [En handling]
- **Förväntat resultat:** [Observerbart, kontrollerbart]

## Otydligheter i kraven
1. ...
2. ...
