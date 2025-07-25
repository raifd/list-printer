
# 📄 Shtesë për Eksportimin në PDF në Ednevnik

Ky userscript shton një buton **"Printoje Listën Evidentuese"** në faqen [ednevnik.edu.mk](https://ednevnik.edu.mk). Kur klikohet, ai gjeneron një PDF të përmbajtjes kryesore të faqes duke përdorur `html2pdf.js`, me margjina të personalizuara dhe ndarje faqesh.

## ✨ Karakteristika

- Shton një buton të pozicionuar në fund të djathtë të faqes.
- Ngarkon automatikisht bibliotekën e nevojshme `html2pdf.js`.
- Gjen dhe eksporton përmbajtjen kryesore (elementë me ID që fillon me `main-`) si PDF.
- Përfshin:
  - Margjinë të sipërme për seksionin e parë.
  - Ndarje faqeje pas seksionit të parë.
  - Layout të pastër të përshtatur për formatin A4.

## 🛠️ Instalimi

Të duhet një menaxhues userscript-i, si:

- [Tampermonkey](https://www.tampermonkey.net/)
- [Violentmonkey](https://violentmonkey.github.io/)
- [Greasemonkey](https://www.greasespot.net/)

Krijo një script të ri dhe ngjite kodin nga [`add-print-button.user.js`](./add-print-button.user.js).

## ✅ Si përdoret

1. Hyr në [ednevnik.edu.mk](https://ednevnik.edu.mk).
2. Shko te një faqe me listë evidente (listë e nxënësve ose notave).
3. Kliko butonin **"Printoje Listën Evidentuese"** që ndodhet poshtë në të djathtë të faqes.
4. Do të shkarkohet automatikisht një skedar PDF me emrin `ednevnik.pdf`.

## 🧩 Varësitë

- [html2pdf.js v0.10.1](https://cdnjs.com/libraries/html2pdf.js/0.10.1) (ngarkohet dinamikisht nga CDN)

## 🗣️ Teksti i Lokalizuar & ⚠️ Kufizime të Njohura

```text
Teksti i butonit:     Printoje Listën Evidentuese
Mesazhi i gabimit:    Printimi nuk është i mundur nga kjo faqe! Ju lutem vizitoni listat evidentuese.

Kufizime:
- Script-i funksionon vetëm në faqet ku përmbajtja kryesore ka një ID që fillon me 'main-'.
- PDF-i merr stilin aktual të faqes në momentin e klikimit — sigurohu që përmbajtja të jetë plotësisht e ngarkuar.
- Disa faqe të Ednevnik mund të mos mbështesin këtë funksionalitet (si faqe raportesh të veçanta).
