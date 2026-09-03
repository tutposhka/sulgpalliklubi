# Ulesanne 2


| № | Rakenduse osa | Klient | Server | Pohjendus |
|---|---|---|---|---|
| 1 | Mangukordade nimekirja kuvamine | X | | Andmete kuvamine toimub brauseris |
| 2 | Kuupaevavalja vorming | X | X | Klient kontrollib mugavuseks, server kontrollib turvalisuseks |
| 3 | "Vabu kohti vahemalt" filtri rakendamine | X | X | Voib filtreerida kliendis, kuid suurte andmemahtude puhul serveris |
| 4 | Kontroll, kas vali on taitmata | X | X | Klient annab kiire tagasiside, server kontrollib loplikult |
| 5 | Kontroll, kas mangukord on juba tais | | X | Ainult server teab tegelikku olukorda |
| 6 | Kontroll, kas kasutaja on sisse logitud | X | X | Klient kuvab olekut, server otsustab |
| 7 | Kontroll, kas kasutaja on admin | | X | Oigusi kontrollitakse alati serveris |
| 8 | Paarikutse saatmine | | X | Tegevus peab olema serveri poolt kinnitatud |
| 9 | Mangutabeli genereerimine ringmeetodiga | | X | Ariloogika kuulub serverisse |
| 10 | Edetabeli arvutamine | | X | Tulemus peab olema usaldusvaarne |
| 11 | Tulemuste sortimine juba laaditud tabelis | X | | Andmed on juba kliendis olemas |
| 12 | Andmebaasi parool | | X | Saladus ei tohi kunagi kliendini jouda |

## Kolm asja, mis ei tohi kunagi kliendile jouda

1. Andmebaasi parool - kasutaja voib seda naha ja kuritarvitada
2. API votmed - neid saab kasutada teenuste vastu
3. Serveri salajased votmed ja tokenid - neid kasutatakse autentimiseks

## Kolm runnakut

| Runnak | Kuidas | Miks serveripoolne kontroll aitab |
|---|---|---|
| Admini oiguste votltsimine | Kasutaja muudab kliendis andmeid. | Server kontrollib tegelikke oigusi |
| Vormipiirangute eemaldamine | HTML-i ja JavaScripti muudetakse DevToolsiga. | Server valideerib andmed uuesti |
| Otsene API paring | Paring saadetakse Postmaniga ilma kasutajaliideseta. | Server kontrollib autentimist ja reegleid |