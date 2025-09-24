Ensin avasin virtuaalikoneen ja menin NameCheapin sivuille, koska halusin vuokrata heiltä minun domain nimen. Lisäsin sivulle tarvittavat tiedot ja päädyin vuokraamaan vuodeksi sivun testinimi.xyz.

<img width="867" height="562" alt="image" src="https://github.com/user-attachments/assets/49f443ea-e1d5-4260-a3b5-07772971b72d" />

Lisäsin IP osoitteen NameCheapin sivuille domainin Advanced Dns kohtaan ja vaihdoin "Type" kohdan A tietueeksi, jotta domainini toimii.

<img width="928" height="402" alt="image" src="https://github.com/user-attachments/assets/bf58db0a-098b-4591-ba9d-554c3296a1d3" />

Seuraavaksi käytin sudo nanoa ja muokkasin tiedostoa näin:

<img width="1020" height="667" alt="image" src="https://github.com/user-attachments/assets/8a97f9c1-f394-4d0c-ba3d-ec902cb2b0e3" />


Jatkoin tehtävän seuraavaan vaiheeseen, eli alidomainien tekemiseen. Kirjauduin takas NamaCheapiin ja menin kohtaan Advanced DNS. Sinne lisäsin kaksi alidomainia "linuxkurssi" ja "toinenalidomain".
Tein toisesta A-tietueen ja toisesta CNAME tietueen.

<img width="910" height="324" alt="image" src="https://github.com/user-attachments/assets/83afa530-eccd-4bb5-a865-fa8a4a6198e9" />

<img width="1161" height="656" alt="image" src="https://github.com/user-attachments/assets/3b9fdfc8-9c04-4c68-8588-94dc8b474a6e" />

<img width="1159" height="647" alt="image" src="https://github.com/user-attachments/assets/897f59fb-1377-43c8-ab71-3dfcd252c374" />

Testasin selaimessa, että molemmat alidomainit toimii hyvin, niinkun yllä kuvissa näkyy.


Seuraavaksi tutkin omaa domainiani testinimi.xyz "host" komennolla. Tälläinen vastaus tuli:

<img width="744" height="120" alt="image" src="https://github.com/user-attachments/assets/0d5a9cfa-4602-49f2-95e4-94beb0064691" />

Ylimmältä riviltä näkee minun domainin nimen ja IP osoitteen.

Tein suraavaksi komennon dig testinimi.xyz

<img width="701" height="397" alt="image" src="https://github.com/user-attachments/assets/e5eaac84-f8e2-4aec-9110-c48b4db3263e" />

Answer kohdassa näkyy domainin nimi ja 1800 tarkoittaa NameCheapin asetusta 30min. Rivin lopussa näkyy IP osoite.
Lisäsin NS pyyntöni perään ja sain lisää vastauksia.

<img width="795" height="408" alt="image" src="https://github.com/user-attachments/assets/bb22db0a-8b67-41c0-879a-2cb1a50f47bc" />

Answer sectionissa näkyy NameCheapin osoitteet rivin lopussa, joka kertoo siitä, että nimi on vuokrattu NameCheapiltä.

Tein samat komennot Supercellin domain nimelle.

<img width="809" height="587" alt="image" src="https://github.com/user-attachments/assets/7b4b0323-9ffb-4b80-a90b-784b8c07ec37" />

Supercellillä on asetettu neljä eri IP osoitetta, kun taas minun sivullani oli yksi. Myös Answer sectionista näkee, että sivut on vuokrattu eri paikoista domain nimien päätteiden perusteella.
Heidän sivuja hoitaa myös barracudanetworks.com.

Viimeiseksi katsoin vielä pienemää yritystä Höyrytys OY. Tein taas samat komennot.


<img width="774" height="519" alt="image" src="https://github.com/user-attachments/assets/0cbeb96c-8cc0-411f-a61a-edc65a56661f" />

Tästä näkee, että heillä on kaksi IP osoitetta merkitty sivulle, kun taas Supercellillä oli neljä ja minulla yksi. Heidän Answer sectionissa ei ole domainia, josta he olisivat voineet vuokrata nimen vaan pelkkä IP osoite.


Lähteet: https://terokarvinen.com/linux-palvelimet/, https://hoyrytys.fi/, https://supercell.com/en/, https://phoenixnap.com/kb/linux-dig-command-examples, https://www.wix.com/blog/what-is-a-subdomain?utm_source=bing&utm_medium=cpc&utm_campaign=506190438^1262241004716722^search%20-%20dsa&experiment_id=wix.com%2Fblog^b^^&msclkid=a9b1ee2779b2115e0c0686f48780b52a,
https://www.geeksforgeeks.org/linux-unix/host-command-in-linux-with-examples/.








