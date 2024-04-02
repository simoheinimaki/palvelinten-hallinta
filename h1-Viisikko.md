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

otetaan ensin ssh yhteys:  $ vagrant ssh

Sen jälkeen voidaan asentaa salt :  sudo apt update  sudo apt install salt-master salt-minion

## Lähteet
Tehtäväsivu: https://terokarvinen.com/2024/configuration-management-2024-spring/#h0-hello

Run Salt Command Locally: https://terokarvinen.com/2021/salt-run-command-locally/

Create a Web Page Using Github: https://terokarvinen.com/2023/create-a-web-page-using-github/

Raportin kirjoittaminen: https://terokarvinen.com/2006/06/04/raportin-kirjoittaminen-4/


