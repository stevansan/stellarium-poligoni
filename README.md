## **Dodavanje LMG poligona u Stellarium**

Počevši od verzije Stellarium-a 0.16.1 (2016. godina), prisutna je opcija sazvežđa i asterizama kao dva odvojena layer-a. LMG poligoni su u Stellarium su implementirani kao layer asterizama.

Da bi ste ih ubacili u Stellarium, potrebno je da arhivu **poligoni.zip** raspakujete u instalacioni direktorijum na lokaciji:  


**Windows** ->  **`C:\Program Files\Stellarium\skycultures\poligoni`**

**Linux** ->  **`/usr/share/stellarium/skycultures/poligoni`**

![Izgled instalacionog direktorijuma sa poligonima na Windows-u](https://lh5.googleusercontent.com/SUC8v9i_FzVRUxTQDJJD7hRORlIKIQRRmkks1OiFEMVqQvxbuOWg1QEK2USXqT-ft8nbQr5zMkeRi5kP8H4S=w1920-h910)

**Slika** **1** Izgled instalacionog direktorijuma sa poligonima na Windows-u

Nakon kopiranja foldera poligoni u Stellarium direktorijum, potrebno je sazvežđa prebaciti na LMG poligone (koji uključuju standardna sazvežđa i poligone kao asterizme).

U Stellariumu izabrati **Sky and viewing options window** -> **Starlore** i iz liste izabrati opciju **LMG poligoni.**

![Izgled instalacionog direktorijuma sa poligonima na Linux-u](https://lh6.googleusercontent.com/9bLEPiTrwIWYP_Ui0Xh_CXeJAetHJmx08JdXkLl0a3DblnFNUeFwe7lSZobfLF7ERLIeNSQ5P_5nU-YxiyMJ=w1920-h910)

**Slika** **2** Izgled instalacionog direktorijuma sa poligonima na Linux-u

![Izgled menija Sky and viewing options, opcija Starlore sa selektovanim LMG poligonima](https://lh3.googleusercontent.com/Uw0ioJsHZZaxxQwLZtbDh-Tz3A04IErXEfldVSx4Ys63BC7Qnr0WWVmQycOjXb5dgqLd-F5SJ_5Q7h2-AVPz=w1920-h910)

**Slika** **3** Izgled menija **Sky and viewing options**, opcija **Starlore** sa selektovanim LMG poligonima



----------
Prilikom dodavanja foldera u Linuxu u sistemski direktorijum nije moguć direktni copy/paste pa je najlakše folder poligoni raspakovati na Desktop i koristiti komandu za pomeranje **mv**  u terminalu:

**`sudo mv /home/vaš-username/Desktop/poligoni /usr/share/stellarium/skycultures/poligoni`**

  
  
## **Napredno – kako se menjaju fajlovi koji definišu asterizme i sazvežđa**

Skyculture opcija sastoji se iz dva layer-a – Constellation i Asterism. Fajlovi koji definišu jedan skyculture su:

- **asterism_lines.fab** – fajl u kome se definišu linije asterizama (definisano HIP oznakama zvezda i parovima koji definišu jednu       liniju)
- **asterism_names.eng.fab** – fajl u kome se definišu imena asterizama
- constellation_names.eng.fab
- constellationsart.fab
- constellationship.fab
- **description.en.utf8** – fajl sa opisom koji se vidi u Stellariumu u Starlore meniju
- **info.ini** – fajl koji definiše naziv skyculture-a
- **reference.fab** – fajl u kome su reference za dati skyculture
- star_names.fab
- PNG slike sazvežđa

Boldovani i opisani su fajlovi koje je bilo potrebno izmeniti kako bi se dodali poligoni kao asterizmi. Na sličan način se menjaju i definicije sazvežđa.


| ![Definicije imena oblasti](https://lh4.googleusercontent.com/SI96Q-lK4ibuEoeJj5O2J38eXtjoRflC6vRAfYy61GoECpPGEmfPCa0OtgF56kXFTU7-ZY2vGBLtaxbq6adp=w1920-h910) | ![Definisanje linija koje ograničavaju poligon](https://lh3.googleusercontent.com/rjequq9uFCr8msaCY1tAVfrNi_WT-i2rh3icl_VW1H2KFSMms3QFrHGUiC8r6zykMohqWe8uRuxYgrCQUJo6=w1920-h910) | 
|--|--|
|  **Slika 4.1** Definicije imena oblasti | **Slika 4.2** Definisanje linija koje ograničavaju poligon |

Na slici 4 prikazani su fajlovi kojima su definisane oblasti. Na slici 4.2 prva kolona su nazivi promenljive datog asterizma. Druga kolona klasa objekta u Skyculture-u (1 – asterism). Treća kolona predstavlja broj zvezda koje definišu dati asterizam. Četvrta kolona su linije asterizma definisane preko HIP oznaka graničnih zvezda:

| O1 | 1 | 4 | 94376 89937 | 89937 83895 | 83895 87585 | 87585 94376 |
|--|--|--|--|--|--|--|
| ID oblasti |  | Broj linija | 1. linija | 2. linija | 3.linija | 4.linija |
