# Tempo: release checklist

Stan na 17.10.2026. Strona główna gotowa (bashubb.com/tempo/), karta podglądu linku zrobiona. **Brakuje privacy i support.**

## Blokuje wydanie
- [ ] **Privacy Policy**: `docs/privacy/index.html` nie istnieje (bashubb.com/tempo/privacy/ zwraca 404). App Store Connect wymaga adresu. Fakty z kodu: brak sieci, import z Photos i Files, wszystko zostaje na iPhonie; do potwierdzenia: zakupy (RevenueCat?), analityka.
- [ ] **Support**: `docs/support/index.html` też brak. FAQ: obsługiwane formaty, eksport, prędkości 0.5×–4×, iOS 17+, tylko iPhone.
- [ ] Po dodaniu: przebudować je skryptem `subpages.py` (ten sam pasek, menu, stopka), dodać linki w stopce i oba adresy do `docs/sitemap.xml` (dziś jest tam tylko strona główna).

## Do potwierdzenia z aplikacją
- [ ] Model płatności: strona nie mówi nic o cenie. Czy ma mówić (jak Wipe: darmowe próby + jednorazowy zakup)?
- [ ] Fakty na stronie: 0.5× do 4×, iOS 17, tylko iPhone, import z Photos i Files, brak sieci.

## Opcjonalnie
- [ ] Film motion graphics na start strony w telefonie (jak Wipe, Ringbox, Mirrorly). Dziś Tempo zaczyna od zapętlonego tła z klipem.

## Na stronie (wszystko w `docs/`)
- [ ] Link do App Store: podmień `https://apps.apple.com/us/search?term=…` na adres aplikacji (`…/app/idXXXXXXXXXX`) we wszystkich `data-store-link` (index, privacy, support).
- [ ] `<html data-store="soon">` → `"live"` w `index.html`. Jednym ruchem zamienia „Coming soon” na odznakę App Store w pasku, hero, stopce.
- [ ] Baner Safari: `<meta name="apple-itunes-app" content="app-id=XXXXXXXXXX">` w `<head>` strony głównej.
- [ ] JSON-LD `SoftwareApplication`: dodać/poprawić `offers` (cena lub usunąć) i link do App Store.
- [ ] Podbić `?v=` przy zmienionym CSS/JS, wypchnąć, sprawdzić na żywo: desktop, telefon pionowo, telefon poziomo.
- [ ] Odpalić `fit-audit.js` (desktop) i `phone-audit.js` (telefony) ze skilla `bashubb-app-sites` → „ALL … FIT”.

## bashubb.com (repo `Bashubb`)
- [ ] Przenieść kartę Tempo z sekcji **Coming soon** do **Available now**, dodać odznakę App Store z linkiem.
- [ ] Dodać Tempo do JSON-LD (`@graph`, jak Shrink) i do `sitemap.xml`.

## App Store Connect
- [ ] Privacy Policy URL: `https://bashubb.com/tempo/privacy/`
- [ ] Support URL: `https://bashubb.com/tempo/support/`
- [ ] Marketing URL: `https://bashubb.com/tempo/`
