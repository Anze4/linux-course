Tiivistelmä

- Apachen avulla samassa IP osoitteessa voi olla useita domain nimiä.
- Kaikki pyynnöt, jotka ei mätsää olemassa olevan virtualhostin kanssa, niin hoidetaan käyttöjärjestelmän avulla.
- Default vhost on hyvä tehdä ensimmäisenä.
- Asennus ja oletussivut luodaan näillä komennoilla: sudo apt-get -y install apache2, echo "default" | sudo tee /var/www/html/index.html


Avasin virtuaalikoneen ja latasin Apachen ja testasin että se toimii. Käytin näitä komentoja: "sudo apt-get update" ja "sudo apt-get install -y apache2" 
<img width="952" height="681" alt="image" src="https://github.com/user-attachments/assets/0e7b4354-c513-42bc-be0d-0ea527bbf7cf" />

Testasin localhost osoitetta nettipalvelimella ja curl komennolla.
<img width="1178" height="795" alt="image" src="https://github.com/user-attachments/assets/bc808cf8-ab9d-472e-bf2c-6c60f39442de" />
<img width="1168" height="455" alt="image" src="https://github.com/user-attachments/assets/9674c95e-ca01-4897-80bc-d7e1fdc1cac6" />

Seuraavaksi avasin lokin tällä komennolla: sudo tail -n 10 /var/log/apache2/access.log.
<img width="1269" height="229" alt="image" src="https://github.com/user-attachments/assets/d5cdd96c-7fb1-4d93-9d92-df56fe752762" />

Rivit 1-3 kertovat, että IP osoite on sama kuin localhostin. Niissä näkyy myös kellonajat milloin pyynnöt localhostin avaamiseen on tehty.
Näkee myös, että pyynnöt on tehty curl komennolla sekä siirtyvien tavujen määrän.
Rivi 4 Näyttää pyynnön Firefox selaimesta ja se näyttää, että yhteys localhostiin on onnistunut.
Rivi 5 kertoo, että Apache kuvatiedosto on haettu automaattisesti Apachen sisältöön.
Rivi 6 sanoo, että selain yritti löytää jotain tiedostoa, mutta sitä ei löytynyt.

Seuraavaksi tein uuden name based virtual hostin nimeltä kenka.example.com. Taistelin tämän vaiheen kanssa pitkään, mutta sain kohdan suoritettua.
Ensin käytin mkdir -p komentoa ja tämän jälkeen nanon ja sudo nanon avulla loin uuden nimen. Tämän jälkeen taistelin pitkään, koska localhost näytti forbidden virheviestiä,
joten en ole varma kaikesta järjestyksestä, että mitä tein. Kuvassa on kuitenkin omaa tehtävän ratkomistani ja toimiva sivu.
<img width="807" height="448" alt="image" src="https://github.com/user-attachments/assets/dccb09ec-21bd-40d2-897b-27be55a96442" />
<img width="1287" height="760" alt="image" src="https://github.com/user-attachments/assets/f506f767-af24-48fe-a4de-d455d658f819" />

Kokeilin seuraavaksi curl ja curl -I komentoja:
<img width="489" height="223" alt="image" src="https://github.com/user-attachments/assets/27143c2c-b50d-487a-a734-e341f146f8d6" />
<img width="355" height="93" alt="image" src="https://github.com/user-attachments/assets/790e0ee4-43a5-4d04-a6f6-7a88fa045628" />

Curl -I komennosta näkee, että sivusto on vastannut onnistuneesti. date kohdasta näkee päivämäärän, kun vastaus on tapahtunut. 
Otsakkeista näkee myös, että mikä serveri vastasi (Apache) ja että se sisältää html tekstiä.




Lähteet:  https://terokarvinen.com/linux-palvelimet/, https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-27082925.md, https://httpd.apache.org/docs/2.4/vhosts/name-based.html







