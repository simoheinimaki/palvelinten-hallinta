# H2

## Tiivistelmät

Karvinen 2021: Two Machine Virtual Network With Debian 11 Bullseye and Vagrant: https://terokarvinen.com/2021/two-machine-virtual-network-with-debian-11-bullseye-and-vagrant/

Karvinen 2018: Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux: https://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/?fromSearch=salt%20quickstart%20salt%20stack%20master%20and%20slave%20on%20ubuntu%20linux

Karvinen 2014: Hello Salt Infra-as-Code: https://terokarvinen.com/2024/hello-salt-infra-as-code/

## Tehtävät
Suoritan tehtävät tietokoneellani Ubuntu serverissä.

### a) Kaksi virtuaalikonetta samassa verkossa

Käytän ohjeenani tekstiä: Karvinen 2021: Two Machine Virtual Network With Debian 11 Bullseye and Vagrant

Ensimmäisenä asennan vagrantin ja virtualboxin

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/2292bde6-d9c8-4b6a-8485-833e5ada12c0)

Sitten luon hakemiston johon luon Vagrantfile tiedoston ohjeiden mukaan

    mkdir twohost/; cd twohost/
    nano Vagrantfile
Kopioin skriptin Vagrantfile tiedoston sisälle ja pääsen käynnistämään ympäristön komennolla 

    vagrant up

Tässä vaiheessa tulee oletettu virhe viesti IP osoitteista.

  ![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/0c8c412c-948d-4368-810e-0ef8c01d37f6)

Korjaan tämän vaihtamalla t001 ja t002 koneen ip osoitteet osoitetun avaruuden sisälle.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/41d7ff03-1cd9-46e0-91b3-f63e6aa1bea8)

Nyt yrittäessä käynnistystä uudestaan se onnistuu ja voin ottaa ssh yhteyden jompaankumpaan koneista ja yrittää pingaamista.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/57769bb4-36fb-4ea8-ada5-d01c20ae0622)

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/22687f2f-4b99-4f62-8cd9-1e1d2e8ee977)

Pingaaminen onnistui.

### b) Herra-orja arkkitehtuuri

en saa toimimaan.








