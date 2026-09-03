# Ulesanne 3

## 1. https://klubi.example.ee:8443/mangukorrad/12?sort=kuupaev&vabu=2#tulemused

| Osa | Vaartus | Mida utleb |
|------|---------|------------|
| Skeem | https | Kasutatakse HTTPS protokolli |
| Host | klubi.example.ee | Millise serveriga suheldakse |
| Port | 8443 | Teenus kuulab pordil 8443 |
| Tee | /mangukorrad/12 | Soovitud ressurss |
| Paringustring | sort=kuupaev&vabu=2 | Filtreerimine ja sorteerimine |
| Fragment | tulemused | Lehe sisene asukoht, serverini ei joua |

Tegelik port: 8443

---

## 2. http://localhost:3000/api/mangijad

| Osa | Vaartus | Mida utleb |
|------|---------|------------|
| Skeem | http | Kasutatakse HTTP protokolli |
| Host | localhost | Kohalik arvuti |
| Port | 3000 | Rakendus kuulab pordil 3000 |
| Tee | /api/mangijad | Mangijate API aadress |
| Paringustring | - | Puudub |
| Fragment | - | Puudub |

Tegelik port: 3000

---

## 3. https://www.ut.ee/et/oppimine?utm_source=uudiskiri

| Osa | Vaartus | Mida utleb |
|------|---------|------------|
| Skeem | https | Kasutatakse HTTPS protokolli |
| Host | www.ut.ee | Tartu Ulikooli veebiserver |
| Port | 443 | HTTPS vaikimisi port |
| Tee | /et/oppimine | Oppimise leht |
| Paringustring | utm_source=uudiskiri | Turunduse ja statistika parameeter |
| Fragment | - | Puudub |

Tegelik port: 443

---

## Millised osad jouavad serverini

| Osa | Jouab serverini | Selgitus |
|------|----------------|-----------|
| Skeem | Jah | Server saab teada kasutatava protokolli |
| Host | Jah | Server peab teadma, millisele hostile paring saadeti |
| Port | Jah | Maarab teenuse, kuhu uhendus luuakse |
| Tee | Jah | Maarab soovitud ressursi |
| Paringustring | Jah | Sisaldab filtreid ja parameetreid |
| Fragment | Ei | Fragment jaab ainult brauserisse |