# H2

## Tiivistelmät

Karvinen 2021: Two Machine Virtual Network With Debian 11 Bullseye and Vagrant: https://terokarvinen.com/2021/two-machine-virtual-network-with-debian-11-bullseye-and-vagrant/

Karvinen 2018: Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux: https://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/?fromSearch=salt%20quickstart%20salt%20stack%20master%20and%20slave%20on%20ubuntu%20linux

Karvinen 2014: Hello Salt Infra-as-Code: https://terokarvinen.com/2024/hello-salt-infra-as-code/

## Tehtävät
Suoritan tehtävät tietokoneellani Ubuntu serverissä.
### Kaksi virtuaalikonetta samassa verkossa
Ensimmäisenä asennan vagrantin ja virtualboxin

![Kuva1](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/0927cd92-a601-45b0-afbf-cdfd3c1672a4)

![Kuva2](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/33a21ffe-c38c-4ba0-bd33-9b4431abe096)

![Kuva3](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/c602a8bf-c37f-4b8d-b333-aceebd9cf80e)

Sitten luon uuden hakemiston ja lisään sinne Vagrantfile tiedoston, joka luo kaksi virtuaalikonetta.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/6ec7001c-a648-4104-9b87-fdb65af8f15b)

Tässä vaiheessa vaihdan käyttämään ssh yhteyttä PuTTY:llä saadakseni sisällön helpommin kopioitua tiedostoon.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/4d7c87e3-264a-4fc2-a7a5-9a289750a1f7)

Käynnistäessä virtuaalikonetta t001 sain odotetun IP error viestin.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/cdd666d1-b410-4e64-88eb-6c65e0dd1cc6)

Korjaan tämän ongelman vaihtamalla virtuaalikoneiden ip osoitteet oikean osoiteavaruuden sisälle.








