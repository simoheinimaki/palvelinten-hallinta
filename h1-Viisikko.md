# H1

## Tiivistelmät
Run Salt Command Locally: https://terokarvinen.com/2021/salt-run-command-locally/

Create a Web Page Using Github: https://terokarvinen.com/2023/create-a-web-page-using-github/

Raportin kirjoittaminen: https://terokarvinen.com/2006/06/04/raportin-kirjoittaminen-4/

### Run Salt Command Locally
- Salt komentojen ajaminen paikallisesti on hyödyllistä harjoittelussa ja testaamisessa
- Tärkeimmät state funktiot ovat: pkg, file, service, user, cmd
- Saltin asentaminen Debian ja Ubuntu:

  $ sudo apt-get update

  $ sudo apt-get -y install salt-minion

### Create a Web Page Using GitHub
- Luo uusi Repositorio (muista README.md tiedosto). Suositeltu lisenssi: GNU General Public License version 3.
- Kirjoita markdownilla. nimeä tiedosto *nimi.md*
- `commit changes` = Tallenna

### Raportin kirjoittaminen
- Kirjoita raporttia samalla kuin teet työtä.
- Kerro työskentely-ympäristö.
- Tuloksen on oltava toistettavissa.
- Kirjoita täsmällisesti mitä teet.
- Tee raportista helppolukuinen
- Muista lähdeviittaukset

## Tehtävät:
Salt-minion on asennettuna

![Kuva1](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/2e8f31e4-6976-423d-a08d-9103c56e3a6d)

Vagrant on asennettuna

![Kuva2](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/5abe560c-d559-4475-83ae-47b5afa169cf)

### Uuden Linux virtuaalikoneen luominen vagrantilla
Uuden virtuaalikoneeen voi luoda syöttämällä komennon:  $ vagrant init debian/bullseye64

Virtuaalikone käynnistetään komennolla:  $ vagrant init debian/bullseye64

![Kuva3](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/d88c7182-8263-4e48-b3ce-7bffea380db6)

### Saltin asennus virtuaalikoneelle

otetaan ensin ssh yhteys:  vagrant ssh

Sen jälkeen voidaan asentaa salt :  
  sudo apt update  
  
  ![Kuva4](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/b88d5546-3401-40c3-a9b8-27a9a6caa1d2)

  
  sudo apt install salt-master salt-minion

  ![Kuva5](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/2bbf9a10-b685-4a58-976c-dbd8c1a9bf36)

Saltin asennus onnistui. 

### Saltin tilafunktiot
Kokeilen kaikkien tilafunktioiden kohdalla *Run Salt Command Locally* artikkelin esimerkkikomentoja.
#### pkg
![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/9e9bbd9a-432d-4f46-a2e8-24f1349a155a)
![Kuva6](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/a9976a81-0bf1-44a4-ac57-d2e1cedcab5f)

komennon ajettuani huomasin sen epäonnistuneen. Asensin Tree työkalun, jonka jälkeen komento onnistui.

![Kuva7](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/e11e8e0d-051c-4a12-99c7-cfdf9a7866a1)

#### file
Ajoin komennon:  sudo salt-call --local -l info state.single file.managed /tmp/testi 

![Kuva9](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/57f6a91b-4593-4e21-874f-0be7e402ec94)

Komennolla loin uuden tiedoston /tmp/testi.

### service

Ajoin komennon:  sudo salt-call --local -l info state.single service.running apache2 enable=True
![Kuva10](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/26ee3910-c374-4348-aed6-2bcebe7d1a5a)

Tämä epäonnistui, koska Apache2 ei ole valmiiksi asennettuna virtuaalikoneelle.

### user

Ajoin komennon:  sudo salt-call --local -l info state.single user.present simo

Tällä komennolla loin uuden käyttäjän ja uuden groupin.

![Kuva11](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/02cd3a99-bf5b-403f-a311-21d68a0ce31c)

### cmd

Ajoin komennon:   sudo salt-call --local -l info state.single cmd.run 'touch /home/vagrant/testi2.txt' 

Tavoitteena luoda tiedosto nimeltä "testi2" vagrant hakemistoon.

![Kuva12](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/bbd5634e-da29-4151-9a9d-749c7ab30e1b)

Tiedoston luominen komennolla onnistui.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/0b52ccfb-e8f7-4806-a72f-bd79c14c4e80)






## Lähteet
Tehtäväsivu: https://terokarvinen.com/2024/configuration-management-2024-spring/#h0-hello

Run Salt Command Locally: https://terokarvinen.com/2021/salt-run-command-locally/

Create a Web Page Using Github: https://terokarvinen.com/2023/create-a-web-page-using-github/

Raportin kirjoittaminen: https://terokarvinen.com/2006/06/04/raportin-kirjoittaminen-4/


