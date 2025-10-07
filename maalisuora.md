1. Kolme kieltä

Ensimmäisenä kielenä käytin pythonia. Pythonin vahvuus on linuxissa sen helppokäyttöisyys komentorivillä ja se on yleensä valmiiksi asennettu, kuten minulla se oli.
Nanon avulla loin hello.py tiedoston ja muokkasin tekstiä.
<img width="807" height="254" alt="image" src="https://github.com/user-attachments/assets/9212052b-e503-4dc6-9fe8-623f619c6331" />

Näyttää toimivan hyvin, kuten alla kuvassa näkyy.

<img width="536" height="86" alt="image" src="https://github.com/user-attachments/assets/b1183a25-3a26-4c10-be0a-eee672b069c3" />


Toisena kielenä käytin Bashia. Bash on se ohjelma, joka lukee komentoja terminaalissa ja suorittaa niitä. Se on valmiiksi ladattuna Linuxissa.
Nanon avulla loin hello.sh tiedoston ja muokkasin sen sisältöä.

<img width="818" height="228" alt="image" src="https://github.com/user-attachments/assets/7a466e23-fc4b-421c-a87e-05f5ccb40345" />

Tämän jälkeen tein skriptistä suoritettavaa chmod +x komennolla ja tarkistin että onnistuinko. Kuvassa alla näkee, että oikein meni.

<img width="528" height="108" alt="image" src="https://github.com/user-attachments/assets/c976f36b-71f3-48f4-a6d0-bc1e2762f19c" />


Kolmantena kielenä päätin käyttää C:tä, koska se oli minulla jo valmiiksi asennettu. C on vanhempi, mutta tehokas ohjelmointikieli, jolla on esimerkiksi itse Linux kirjoitettu. C toimii siis hyvin luontevasti Linuxissa.

Loin nanon avulla tiedoston hello.c ja muokkasin sitä.

<img width="492" height="206" alt="image" src="https://github.com/user-attachments/assets/179f12ae-862f-4603-a844-5be0ae156fa7" />

Tämän jälkeen muutin hello.c tiedoston suoritettavaksi ohjelmaksi gcc komennon avulla. Eli siitä tuli hello_c. Alla näkyy, että kun ajan ohjelman niin tulee esiin teksti "Hei maailma", joten koodi toimii.

<img width="559" height="162" alt="image" src="https://github.com/user-attachments/assets/08060566-6c18-404b-a100-49db09225c64" />


2. Uusi komento

Päätin luoda komennon, jota käyttämällä ilmestyy teksti Hei maailma. Loin kotihakemistossa tiedoston nano terveiset. Muokkasin tiedostoa sopivaksi, näkyy kuvassa.

<img width="653" height="160" alt="image" src="https://github.com/user-attachments/assets/82b9532f-dab4-4040-b455-b835d7475261" />

Tein tiedostosta mahdollisen suorittaa chmod +x komennolla ja tein terveiset komennosta kaikkien käytettävän sudo mv komennolla. Komennot näkyy vielä alla kuvassa.

<img width="551" height="61" alt="image" src="https://github.com/user-attachments/assets/4ae39dbc-62dd-425f-96b2-ffc941ae2912" />

Testasin vielä terminaalissa, että toimiiko oma tekemä terveiset komento ja alla kuvassa näkyy, että komento toimii.

<img width="325" height="66" alt="image" src="https://github.com/user-attachments/assets/8c9e12ec-65df-4fab-aa58-c05b260c5ce2" />


3. Laboratorioharjoitus

Päätin tehdä tämän laboratorioharjoituksen Linux palvelimet ict4tn021-6 torstai – alkukevät 2018 – 5 op. Päätin soveltaa tehtävää ja tein sen paikallisesti ilman MySQL käyttämistä. Aluksi latasin tehtävään tarvittavat peruspaketit, näkyy alla kuvassa.

<img width="612" height="44" alt="image" src="https://github.com/user-attachments/assets/59e13d6f-2999-45d6-ac9f-80446cc0f842" />

Tämän jälkeen käynnistin Apachen sudo systemctl start apache2 ja sudo systemctl enable apache2. Testasin myös curlilla, että toimiiko apache, ja se toimi.

<img width="796" height="129" alt="image" src="https://github.com/user-attachments/assets/097c9ff9-0ae4-493d-998a-c4914215897d" />

Loin hakemiston tehtävälle sudo mkdir komennolla ja vaihdoin cd komennolla tekemääni uuteen hakemistoon.

<img width="635" height="22" alt="image" src="https://github.com/user-attachments/assets/c2e27e6f-e4a2-44bd-93e2-9bcce6564701" />
<img width="529" height="45" alt="image" src="https://github.com/user-attachments/assets/72f0b300-a44f-4ed4-9882-5aba448da26c" />

Tein komennon nano asiakkaat.json ja muokkasin tiedostoa tarvittavan laiseksi. Lisäsin sinne asiakkaiden nimet ja yhteyshenkilöt.

<img width="767" height="139" alt="image" src="https://github.com/user-attachments/assets/2ac5b97e-f7b3-44fc-a75b-3c66e47e2c61" />

Asiakas tiedoston jälkeen loin php sivun lukemaan asiakas.json tiedoston tiedot. Loin nano index.php ja loin sinne tiedoston, mikä pystyy lukemaan asiakas,json tiedot.

<img width="813" height="485" alt="image" src="https://github.com/user-attachments/assets/a71a66e6-1e2f-4208-9d62-437a577185ff" />

Tein vielä perus apacheen tarvittavan tiedoston sudo nanon ja a2ensite komentojen avulla. Nimet näkyvät localhostissa.

<img width="1253" height="311" alt="image" src="https://github.com/user-attachments/assets/ebb9a257-c1f1-4c8e-b1fa-2bdef362925b" />







