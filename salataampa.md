Tiivistelmä
- Https certifikaatin hankkimisessa ACME-asiakasohjelmaa käyttämällä on kaksi tärkeää vaihetta. Ensin ACME-asiakasohjelma todistaa varmenteelle (CA), että verkkopalvelin hallitsee tiettyä verkkotunnusta. Tämän jälkeen asiakasohjelma voi pyytää tai peruuttaa varmenteita kyseiselle verkkotunnukselle.
- Let’s Encrypt tunnistaa ACME-asiakasohjelmiston julkisen avaimen perusteella.
- Kun asiakasohjelma on valtuutettu, varmenteiden pyytäminen, uusiminen ja peruuttaminen on yksinkertaista. Lähetetään vain varmenteiden hallintaviestit ja allekirjoitetaan ne tilin avainparilla.
- Varmenteen uusiminen myöhemmin tarkoittaa, että myöntämisprosessi toistetaan alusta alkaen. Suoritetaan siis verkkotunnuksen validointi ja sen jälkeen pyydetään uusi varmenne.
- Jos sinulla on olemassa oleva palvelin, joka käyttää porttia 80, http-valinta vaatii myös http.webroot-valinnan.
- .well-known/acme-challenge hakemiston tulisi olla julkisesti saatavilla polkuna kyseisessä verkkotunnuksessa, jotta validointi voidaan suorittaa loppuun. Jos hakemisto ei ole julkisesti saatavilla, sinun on uudelleenkirjoitettava pyynnöt tähän hakemistoon.
- Sinun tulisi pystyä ajamaan olemassa olevaa verkkopalvelinta portissa 80 käyttämällä tätä: lego --accept-tos --email you@example.com --http --http.webroot /path/to/webroot --domains example.com run.
- SSL-asetuksesi tulee sisältää vähintään seuraavat määritykset: <img width="551" height="168" alt="image" src="https://github.com/user-attachments/assets/61fee65d-1100-4763-8e6f-1c970521cb5f" />
