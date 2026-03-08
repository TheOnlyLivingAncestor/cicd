[![Actions Status](https://github.com/TheOnlyLivingAncestor/cicd/workflows/Test,%20build%20and%20release/badge.svg)](https://github.com/TheOnlyLivingAncestor/cicd/actions)
# Labor2: CI/CD környezet kialakítása és alkalmazása
A labor során létrehozott és a munkát tartalmazó ezen projektben a GitHub Actions CI/CD eszközzel fogunk megismerkedni.
## A CI/CD jelentése
A CI/CD a “continuous integration” és “continuous delivery/deployment” rövidítése, vagyis ez a módszer(tan) a folyamatos integrációt és folyamatos szállítást/telepítést jelenti. Azért nevezik gyakran CI/CD “pipeline”-nak ezt, mert ezek egymásra épülő folyamatok és mint a vízvezetékeknél, általában az irány adott.
## A CD/CD környezet céljai
A folyamatos integráció során a fejlesztők a kódjaikat naponta többször egyeztetik (megosztják) egy verziókezelő rendszerben. Ezeken a kódokon – általában automatikus – teszteket futtatnak,amelyek:
megmutathatják a kódrészletek vagy akár az egész alkalmazás fordíthatóságát (persze amelyik nyelvnél van ilyen lépés),
statikus elemzést végeznek a kódon a programozási hibák kiszűrésére (→ lásd lint),
ellenőrzik a kódrészletek (funkcionálisan) helyes működését (→ lásd unit test).
A folyamatos integráció tartalmazza a “build” lépést is, amely során az alkalmazás futtatható változata készül el (forráskód tárgykóddá alakításával, erőforrások linkelésével).

A folyamatos szállítás/telepítés során az alkalmazás a pillanatnyi (de a CI során tesztelésen átment) állapotban kerül ki a “production” környezetbe, akár már egy hiba javításától számítva néhány percen belül is. Az üzemeltetés így sokkal gyorsabban tud visszajelzéseket küldeni, amelyek alapján aztán újabb módosítások kerülhetnek a kódba.

A futtatható állomány [itt](https://github.com/TheOnlyLivingAncestor/cicd/releases/tag/latest) érhető el.