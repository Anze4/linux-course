Tiivistelmä 
- On monta eri vaihtoehtoa pilvipalvelimen vuokraukseen
- Parhaat sivustot maksavat hieman
- Palomuuriin pitää tehdä reikä, jotta portti toimii
-  Palomuurin reikä tehdään komennolla $ sudo ufw allow 22/tpc
-  Palomuuri laitetaan päälle komennolla $ sudo ufw enable
-  Virtuaalipalvelimen käyttäjälle pitää tehdä hyvä salasana, mutta jättää muut kohdat tyhjiksi
-  Lopuksi sivusto pitäisi näkyä chrome selaimessa


Käytin tehtävässä DigitalOcean palvelua. Aluksi kirjauduin github käyttäjän avulla sisään ja sen jälkeen lisäsin palveluun maksutiedot.
Tämän jälkeen menin kohtaan Droplets ja vuokrasin halvimman mahdollisen Debian virtuaalikoneen.
<img width="1266" height="359" alt="image" src="https://github.com/user-attachments/assets/1410649a-eda0-49e7-a949-63ca0cdd35dc" />

Tämän jälkeen avasin virtuaalikoneeni ja terminaalissa loin yhteyden DigitalOceanissa luomaani koneeseen ssh root komennolla.
<img width="812" height="262" alt="image" src="https://github.com/user-attachments/assets/61dffd29-f1b1-44a1-8598-a19aa52bd2de" />

Sitten tein sudo apt-get update ja tämän jälkeen asensin palomuurin komennolla sudo apt-get install ufw.
<img width="793" height="357" alt="image" src="https://github.com/user-attachments/assets/29492f45-2788-4b4c-a900-4329d0fc12a7" />

Tein reiän palomuuriin komennolla sudo ufw allow 80/tpc ja käynnistin palomuurin.
<img width="788" height="139" alt="image" src="https://github.com/user-attachments/assets/badf80c1-0099-4eab-bc7b-03398e346c76" />

Seuraavaksi tein virtuaalipalvelimen. Käytin komentoa sudo adduser aatul. Tein käyttäjästä pääkäyttäjän ja jätin suurimman osan kohdista tyhjäksi.

<img width="769" height="329" alt="image" src="https://github.com/user-attachments/assets/d50265d0-cb32-482c-9b64-1b56a6074d24" />


Tämän jälkeen latasin apache2 palvelimen ja testasin, että palvelin toimii oikein.
<img width="833" height="364" alt="image" src="https://github.com/user-attachments/assets/8f3e61dc-640d-431b-8a63-295f1008acfd" />

Seuraavaksi loin nettisivun näkyviin sudo a2enmod userdir komennon ja echo komennon avulla. Sivu toimi oikein hyvin. En kuitenkaan saa nyt teknisten ongelmien ja koneen vaihdon takia kuvaa lopullisesta sivusta.


Lähteet: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/, https://terokarvinen.com/linux-palvelimet/, https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/, https://www.digitalocean.com/









