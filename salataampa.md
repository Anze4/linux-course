Tiivistelmä
- Https certifikaatin hankkimisessa ACME-asiakasohjelmaa käyttämällä on kaksi tärkeää vaihetta. Ensin ACME-asiakasohjelma todistaa varmenteelle (CA), että verkkopalvelin hallitsee tiettyä verkkotunnusta. Tämän jälkeen asiakasohjelma voi pyytää tai peruuttaa varmenteita kyseiselle verkkotunnukselle.
- Let’s Encrypt tunnistaa ACME-asiakasohjelmiston julkisen avaimen perusteella.
- Kun asiakasohjelma on valtuutettu, varmenteiden pyytäminen, uusiminen ja peruuttaminen on yksinkertaista. Lähetetään vain varmenteiden hallintaviestit ja allekirjoitetaan ne tilin avainparilla.
- Varmenteen uusiminen myöhemmin tarkoittaa, että myöntämisprosessi toistetaan alusta alkaen. Suoritetaan siis verkkotunnuksen validointi ja sen jälkeen pyydetään uusi varmenne.
- Jos sinulla on olemassa oleva palvelin, joka käyttää porttia 80, http-valinta vaatii myös http.webroot-valinnan.
- .well-known/acme-challenge hakemiston tulisi olla julkisesti saatavilla polkuna kyseisessä verkkotunnuksessa, jotta validointi voidaan suorittaa loppuun. Jos hakemisto ei ole julkisesti saatavilla, sinun on uudelleenkirjoitettava pyynnöt tähän hakemistoon.
- Sinun tulisi pystyä ajamaan olemassa olevaa verkkopalvelinta portissa 80 käyttämällä tätä: lego --accept-tos --email you@example.com --http --http.webroot /path/to/webroot --domains example.com run.
- SSL-asetuksesi tulee sisältää vähintään seuraavat määritykset: <img width="551" height="168" alt="image" src="https://github.com/user-attachments/assets/61fee65d-1100-4763-8e6f-1c970521cb5f" />



Tehtävä

Ensin avasin virtuaalikoneen ja menin terminaaliin. Sitten menin ssh rootin avulla oikealle koneelle IP osoitteen avulla. 
Tämän jälkeen latasin certbotin, jonka jälkeen yritin hankkia serifikaatteja domaineille, mutta tuli virheilmoitus.
<img width="1276" height="312" alt="image" src="https://github.com/user-attachments/assets/38f8183c-1a6c-4e20-9fcf-b043ce4d70b5" />

En ymmärtänyt mistä virhe johtui, mutta käytin dig komentoa, jotta saisin lisää tietoa.
<img width="1301" height="417" alt="image" src="https://github.com/user-attachments/assets/b016df18-0861-4139-a2ec-91480efeadcd" />

Ilmeisesti status kohdan NXDOMAIN on ongelma, mutta en tiedä miten sen saa kuntoon. Namecheapilla on kaikki mielestäni kunnossa ja pääsen sivustolleni muillakin laitteilla, mutta en saa certbotin sertifikaatteja.
<img width="1124" height="337" alt="image" src="https://github.com/user-attachments/assets/fed7c035-ecbd-43d7-bb80-22f6f6676d45" />
<img width="1146" height="162" alt="image" src="https://github.com/user-attachments/assets/3f509d5b-551f-400b-ab72-a4e447e314f5" />
<img width="1144" height="134" alt="image" src="https://github.com/user-attachments/assets/91f6f3f7-55fc-49dd-bd89-5cedd8dc12f7" />


En tiedä mistä virhe johtuu. Pitää varmaan seuraavalla tunnilla pyytää apua.


Kokeilin nyt vielä seuraavana päivänä uudestaan ja jostain syystä certbotilla sertifikaatin hankkiminen tällä kertaa onnistui.
<img width="1138" height="270" alt="image" src="https://github.com/user-attachments/assets/a3381ebc-b03e-49bd-b689-273a17acebc2" />

Sivustokin näytti tällä kertaa oikealta! Lukko näkyy ja https.
<img width="947" height="77" alt="image" src="https://github.com/user-attachments/assets/be7411fc-b19a-4847-b92a-f545bebed451" />

Kävin vielä testaamassa sivuni SSL labsin palvelussa ja sain A-ratingin laadunvarmistuksesta, joten hyvin se lopulta meni.
<img width="1108" height="742" alt="image" src="https://github.com/user-attachments/assets/4b2200be-1bae-4e68-90db-375e42e51f5f" />





Lähteet: https://go-acme.github.io/lego/usage/cli/obtain-a-certificate/index.html#using-an-existing-running-web-server, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample, https://letsencrypt.org/how-it-works/, https://github.com/Phoolis/HH-linux-palvelimet/blob/main/h5.md, https://www.ssllabs.com/ssltest/.







