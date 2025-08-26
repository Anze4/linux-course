Harjoitusksen ideana oli siis luoda linux virtuaalikone ja tehdä siihen tarvittavat muutokset. Harjoitus on tehty maanantaina
25.8.2025 iltapäivällä. Koneena toimi harjoituksessa HP merkkinen läppäri. Harjoitus suoritettiin omassa kodissani Helsingissä.

Asennus ja lataus
Aluksi latasin Oracle VirtualBox Managerin tästä linkistä https://www.virtualbox.org/wiki/Downloads. Tämän latauksen jälkeen
latasin Debian ISO Imagen tästä linkistä https://cdimage.debian.org/debian-cd/13.0.0-live/amd64/iso-hybrid/. Kun koneeni oli 
lataukset suorittanut pääsin aloittamaan virtuaalikoneen luomista.

Virtuaalikoneen luominen Linuxiin.
Avasin Oracle VirtualBox Managerin ja pääsin Oraclen aloitussivulle. Painoin vasemmasta yläkulmasta new ja lisäsin tarvittavat
tiedot, jotka näkyy tässä kuvassa
<img width="837" height="295" alt="image" src="https://github.com/user-attachments/assets/d6c1584b-66d0-42d3-91ab-bb5512764ce3" />
Lisäsin systeemiin tallennustilaksi 2048mb ja virtuaalimonitorien määräksi 1. Hard discin kooksi valitsin 20GB ja painoin
"Finish" näppäintä. Olin nyt luonut virtuaalikoneen ja seuraavaksi se pitäisi käynnistää. Alla vielä kuva luodusta 
virtuaalikoneesta Oraclessa. 
<img width="1071" height="903" alt="image" src="https://github.com/user-attachments/assets/d2bf1d49-f9c7-4da4-8604-b191a4ac5ef1" />

Virtuaalikoneen käynnistys
Luulin tehneeni kaiken oikein ja ajattelin yrittää virtuaalikoneen käynnistämistä. Painoin hiiren oikealla painikkeella 
virtuaalikoneesta linux-test1 ja tämän jälkeen start näppäintä. Virtuaalikone yritti käynnistyä hetken aikaa, mutta se ei 
kuitenkaan onnistunut. Yritin kolmesti käynnistää konetta mutta aina tuli sama error viesti ruutuun. Unohdin ottaa error 
viestistä kuvaa. 
Tajusin onneksi, että syy on todennäköisesti UEFI/BIOS asetuksissa. Googletin miten pääsen UEFI/BIOS 
asetuksiin omalla HP merkkisellä koneella ja tämän jälkeen suoritin tarvittavat toimenpiteet, jotta pääsin asetuksiin. 
Omassa koneessani asetuksiin pääsi laittamalla koneen kiinni ja uudelleen käynnistyksen aikana painoin ensin "ESC" ja sitten
"f10". UEFI asetuksen kohdalla painoin "Enable" ja käynnistin koneeni taas uudestaan. Käynnistyksen jälkeen menin takaisin 
Oracle VirtualBox Manageriin ja kokeilin linux-test1 virtuaalikoneen käynnistämistä uudestaan. Tällä kertaa käynnistys 
onnistui ja pääsin virtuaalikoneeseen sisään.

Virtuaalikoneen testaaminen ja reboot
Kun pääsin virtuaalikoneeseen sisään aloin tehdä tarvittavia alku testauksia. Painoin vasemmasta yläkulmasta "Applications" 
painiketta ja sen jälkeen painoin "Web Browser" painiketta, jotta pääsin nettiin. Tein pari hakua web browserissa ja sen
jälkeen palasin koti näytölle. Avasin terminaalin ja kokeilin näppäimistön toimintaa ja erilaisia komentoja. Huomasin, että 
erikoismerkit olivat virtuaalikoneessa asetettu eri paikkoihin, kun mistä ne löytyi näppäimistössäni. Tässä kohtaa en 
tiennyt, että mistä tämä johtui.

Debianin lataaminen virtuaalikoneeseen
Aloitin Debianin lataamisen virtuaalikoneeseen reboottaamalla virtuaalikoneen terminaalissa. Kirjoitin "sudo reboot" komennon,
mutta reboottaus ei onnistunut, vaan tuli tämä virheilmoitus, joka näkyy alla kuvassa
<img width="1918" height="1032" alt="image" src="https://github.com/user-attachments/assets/3e8c1c06-452c-4007-bfd4-de55b76ca757" />.
Suljin virtuaalikoneen ja kävin lisäämässä ISO filen virtuaalikoneen asetuksista. ISO file oli siis lataamani Debian ISO Image.
Avasin virtuaalikoneen uudestaan ja tällä kertaa reboottaus onnistui.

Painoin virtuaalikoneen reboottauksen jälkeen aloitus näytöllä "start installer" painiketta. Tämän jälkeen aloin täyttää
tarvittavia tietoja, jotta Debianin lataaminen onnistuu mutkitta ja hyvin. En muistanut ottaa tästä vaiheesta kuvia, mutta 
tein tarvittavat muutokset Johannan linkissä olleiden ohjeiden mukaan. Kaikki onnistui tässä kohtaa hyvin ja lataus suoriutui
myös mallikkaasti ja ilman ongelmia. Myös erikoismerkit toimivat latauksen jälkeen synkassa näppäimistön ja virtuaalikoneen kanssa.
Alla vielä kuvat kirjautumis näytöstä ja omasta virtuaalikoneen työpöydästä.
<img width="1290" height="808" alt="image" src="https://github.com/user-attachments/assets/2719cf3b-8efd-425a-9ba1-7dd5274d6ea0" />
<img width="1284" height="811" alt="image" src="https://github.com/user-attachments/assets/370ef063-a4ff-4a78-afa1-9d02e155a277" />



Lähteet:
https://terokarvinen.com/linux-palvelimet/
https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md
Debian lataus: https://cdimage.debian.org/debian-cd/13.0.0-live/amd64/iso-hybrid/
VirtualBox lataus: https://www.virtualbox.org/wiki/Downloads
https://hhmoodle.haaga-helia.fi/course/view.php?id=44090&section=0












