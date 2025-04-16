# Opis problema
Tema skupinskega projekta je kolesarjenje v Sloveniji.

V okviru tega raziskovalnega problema bi radi odgovorili na naslednja ključna vprašanja:
- Kateri in kakšni so najbolj popularni segmenti? – Kako zahtevne so najbolj priljubljene poti, kakšne razdalje in višinske razlike običajno premagujejo kolesarji? Gre za cestno, urbano ali gorsko kolesarjenje?
- Kaj je povprečno število voženj po kategorijah vzpona
- Kaj lahko povemo o dolžinah in vzponih poti? – Ali obstaja korelacija med dolžino in vzponom poti, korelacija med dolžino segmenta in številom voženj?
- Katero področje Slovenije je kolesarsko najbolj aktivno - Ali so katere regije bolj aktivne od ostalih?
- Kako se regije razlikujejo po lastnostih svojih običajnih poti? - Ali so morda poti z visokimi vzponi bolj pogosta v nekaterih regijah?
- Kje bi bilo kolesarstvo še posebej vredno spodbujati? – Katera območja zaostajajo?

# Podatki
Za analizo problema črpamo podatke iz aplikacija Strava, kjer svoje vožnje objavljajo tako rekreativni kolesarji kot tudi profesionalci.

Za pridobitev ustreznih podatkov smo uporabili javno dostopen API platforme Strava (https://www.strava.com/api/v3/segments/explore), ki omogoča iskanje kolesarskih segmentov glede na geografsko območje. Zbrane podatke o posameznih segmentih smo shranili v tabelo, kjer so zabeležene informacije, kot so dolžina poti, skupni vzpon, težavnost, število voženj na segmentu ter relativna priljubljenost posameznega segmenta.
Ta baza služi kot osnova za nadaljnjo analizo, primerjavo med regijami in oblikovanje zaključkov.

Prvotne podatke smo prejeli kot json datoteko, vendar smo jih za lažjo uporabo predelali v datoteko *segmenti.csv*.

# Analiza in glavne ugotovitve
## Kateri segmenti so najbolj priljubljeni?

Najbolj priljubljen segment se pojavi le 6-krat, hkrati pa so ostali popularni segmenti obiskani le 2-krat, kar namiguje na relativno majhno količino podatkov.

![najbolj_priljubljenih_segmentov](https://github.com/user-attachments/assets/2a0c4574-2836-454f-965c-70de3fcc7636)


Segmenti brez vzpona so bolj pogosti, različne kategorije vzponov pa so si med sabo podobno priljubljene.

![števila_voženj_po_kategorijah_vzpona](https://github.com/user-attachments/assets/b96076fb-7c3b-40e7-8a6d-2f968a57e481)



## Katere dolžine segmentov so najpogostejše?

Večina segmentov je krajših od 10km.

![porazdelitev_dolzin](https://github.com/user-attachments/assets/277c1392-4d10-41b3-9f2d-39d7a5157122)

## Katere regije so najbolj aktivne?

Za oceno aktivnosti regij primerjamo število segmentov v posamezni regiji.

![top10_regij_segmentov](https://github.com/user-attachments/assets/bdb161e1-d990-4e03-a8d2-e8692d47adc1)

## Kateri segmenti imajo največjo višinsko razliko?

Največja višinska razlika segmenta presega 1500m.

![top10_vzponi_nov](https://github.com/user-attachments/assets/96f21c20-3e07-462e-a49e-6ae2b9b6dc67)












Če razdelimo segmente po kategoriji vzpona, opazimo da so povprečni nakloni večji za strmejše vzpone.

![graf3_boxplot_naklon_kategorije](https://github.com/user-attachments/assets/a7f97689-a3ee-488d-99fe-a364e17d7ac1)

## Katero področje Slovenije je kolesarsko najbolj aktivno?

Razporeditev po Sloveniji je precej enakomerna, 

![graf4_geografske_tocke_map](https://github.com/user-attachments/assets/a9e1efbb-94f6-4b1e-a2c3-c9876b4ca8fa)


razvidno pa je tudi, da se v Zagrebu začne nadpovprečno število poti.

![heatmap_aktivnost_zemljevid](https://github.com/user-attachments/assets/1671a8f8-c7be-4d3f-8faa-820f58ed3867)






