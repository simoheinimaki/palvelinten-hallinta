# H2

## Tiivistelmät

Karvinen 2021: Two Machine Virtual Network With Debian 11 Bullseye and Vagrant: https://terokarvinen.com/2021/two-machine-virtual-network-with-debian-11-bullseye-and-vagrant/

Karvinen 2018: Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux: https://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/?fromSearch=salt%20quickstart%20salt%20stack%20master%20and%20slave%20on%20ubuntu%20linux

Karvinen 2014: Hello Salt Infra-as-Code: https://terokarvinen.com/2024/hello-salt-infra-as-code/

### Two Machine Virtual Network With Debian 11 Bullseye and Vagrant

- Ubuntulle ja Debianille vagrantin ja virtualboxin asentaminen komennoilla:

      sudo apt-get update
      sudo apt-get install vagrant virtualbox

- Windows ja Mac -> installer
- Luo hakemisto  "twohost"  ja Konfigurointi tiedosto "Vagrantfile" joka sisältää skriptin kahdelle virtuaalikoneelle.

        # -*- mode: ruby -*-
        # vi: set ft=ruby :
        # Copyright 2019-2021 Tero Karvinen http://TeroKarvinen.com
        
        $tscript = <<TSCRIPT
        set -o verbose
        apt-get update
        apt-get -y install tree
        echo "Done - set up test environment - https://terokarvinen.com/search/?q=vagrant"
        TSCRIPT

        Vagrant.configure("2") do |config|
        	config.vm.synced_folder ".", "/vagrant", disabled: true
        	config.vm.synced_folder "shared/", "/home/vagrant/shared", create: true
        	config.vm.provision "shell", inline: $tscript
        	config.vm.box = "debian/bullseye64"

        	config.vm.define "t001" do |t001|
        		t001.vm.hostname = "t001"
        		t001.vm.network "private_network", ip: "192.168.88.101"
        	end

	        config.vm.define "t002", primary: true do |t002|
        		t002.vm.hostname = "t002"
        		t002.vm.network "private_network", ip: "192.168.88.102"
        	end
	
        end
- Ota ssh yhteys

      vagrant ssh t001
- Koneet voivat pingata toisiaan

        vagrant ssh t001
        vagrant@t001$ ping -c 1 192.168.88.102
        vagrant@t001$ exit

        vagrant ssh t002
        vagrant@t002$ ping -c 1 192.168.88.101
        vagrant@t002$ exit

-Tuhoa ja luo uudet virtuaalikoneet

    vagrant destroy
    vagrant up

### Salt Stack Master and Slave on Ubuntu Linux

- Masterin asennus

        master$ sudo apt-get update
        master$ sudo apt-get -y install salt-master

- Salli palomuurissa portit 4505/tcp ja 4506/tcp
- Asenna toiselle koneelle Minion

        master$ sudo apt-get update
        master$ sudo apt-get -y install salt-minion

- Määritä Minionissa Masterin sijainti

      sudoedit /etc/salt/minion

- Restarttaa salt minion daemon

        systemctl restart salt-minion.service

- Hyväksy masterissa "slavekey"

        master$ sudo salt-key -A

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








