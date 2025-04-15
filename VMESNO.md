# Opis problema
Tema skupinskega projekta je kolesarjenje v Sloveniji.

V okviru tega raziskovalnega problema bi radi odgovorili na naslednja ključna vprašanja:
- Kateri in kakšni so najbolj popularni segmenti? – Kako zahtevne so najbolj priljubljene poti, kakšne razdalje in višinske razlike običajno premagujejo kolesarji? Gre za cestno, urbano ali gorsko kolesarjenje?
- Kaj lahko povemo o dolžinah in vzponih poti? – Ali obstaja korelacija med dolžino in vzponom poti?
- Katero področje Slovenije je kolesarsko najbolj aktivno?
- Kako se območja razlikujejo po lastnostih svojih običajnih poti? - Ali so morda poti z visokimi vzponi bolj pogosta v določenih območjih?
- Kje bi bilo kolesarstvo še posebej vredno spodbujati? – Katera območja zaostajajo po infrastrukturi, zanimanju ali dostopnosti?

# Podatki
Za analizo problema črpamo podatke iz aplikacija Strava, kjer svoje vožnje objavljajo tako rekreativni kolesarji kot tudi profesionalci.

Za pridobitev ustreznih podatkov smo uporabili javno dostopen API platforme Strava (https://www.strava.com/api/v3/segments/explore), ki omogoča iskanje kolesarskih segmentov glede na geografsko območje. Zbrane podatke o posameznih segmentih smo shranili v tabelo, kjer so zabeležene informacije, kot so dolžina poti, skupni vzpon, težavnost ter relativna priljubljenost posameznega segmenta.
Ta baza služi kot osnova za nadaljnjo analizo, primerjavo med regijami in oblikovanje zaključkov.

Prvotne podatke smo prejeli kot json datoteko, vendar smo jih za lažjo uporabo predelali v datoteko *segmenti.csv*.

# Analiza in glavne ugotovitve
## Kateri segmenti so najbolj popularni?

Večina segmentov je krajših od 2Km.

![graf1_histogram_dolzina](https://github.com/user-attachments/assets/2ddf1386-d50e-4d4d-9063-348489d322ca)


Ob opazovanju spodnjega grafa je videti, da:
- največ segmentov nima vzpona,
- so segmenti z večjimi vzponi vedno bolj redki,
- obstaja korelacija med dolžino segmenta in vzponom - daljši kot je segment, večji je vzpon.
  
![graf2_scatter_dolzina_vs_visina](https://github.com/user-attachments/assets/b66106d4-92b6-48fa-8af8-80b145bc2b8d)


Število segmentov res pada z zahtevnostjo vzpona:

![graf5_frekvenca_kategorij](https://github.com/user-attachments/assets/67fc87cb-b9ef-4f2b-b0df-5b86a9ae3b70)


Če razdelimo segmente po kategoriji vzpona, opazimo da so povprečni nakloni večji za strmejše vzpone.

![graf3_boxplot_naklon_kategorije](https://github.com/user-attachments/assets/a7f97689-a3ee-488d-99fe-a364e17d7ac1)

## Katero področje Slovenije je kolesarsko najbolj aktivno?

Razporeditev po Sloveniji je precej enakomerna, 

![graf4_geografske_tocke_map](https://github.com/user-attachments/assets/a9e1efbb-94f6-4b1e-a2c3-c9876b4ca8fa)


razvidno pa je tudi, da se v Zagrebu začne nadpovprečno število poti.

![heatmap_aktivnost_zemljevid](https://github.com/user-attachments/assets/1671a8f8-c7be-4d3f-8faa-820f58ed3867)






