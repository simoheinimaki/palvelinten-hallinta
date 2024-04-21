# H3 

## Tiivistelmät

### Pro Git, 2ed: 1.3 Getting Started - What is Git?

- Isoin ero Gitin ja muiden versionhallinta työkalujen välillä on se miten Git käsittelee dataa.
- Suurin osa toiminnoista, kuten projektihistorian tarkastelu käyttävät vain paikallisia resursseja.
- Suurelta osin Git toimii ilman verkkoyhteyttä.
- Tiedostoja ei voi poistaa tai korruptoida ilman, että Git tietäisi niistä.
- Kolme päätilaa: modified, staged ja committed.

### git add . && git commit; git pull && git push.

- "git add ." Lisää nykyiseen hakemistoon tehdyt muutokset seuraavaan tallennukseen.
- "&&" Suorittaa seuraavan komennon jos aikaisempi onnistui.
- "git commit" Tallentaa repositorion
- ";" Mahdollistaa monen komennon ajon peräkkäin
- "git pull" Hakee muiden tekemät muutokset ja päivittää repositorion.
- "git push" Päivittää ulkoisen repositorion

#### Lähteet

Git Guides. Luetavissa: https://github.com/git-guides/git-push . Luettu 15.4.

###


## Tehtävät

### a) Online

Uusi varasto

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/b9203114-9169-4f29-845e-0321d7b16e46)

### b) Dolly

Tein uuden varaston Git Hubissa ja kloonasin sen 

    git clone https://github.com/simoheinimaki/repo-summer

Loin varastoon uuden tekstitiedoston gitissä nanolla 

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/c478f724-acc0-4bd3-b00f-8791b6a82fcf)

Sitten tallennan muutokset varastoon.

    git add . && git commit; git pull && git push

Lisään commit messagen

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/0c34c493-ef5f-41af-be4d-fd6c2c4bed98)

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/f8630560-455e-4e3d-95d6-de299784986a)

Nyt uusi tiedosto näkyy Git Hubissa

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/c5e782d5-b5a9-47c4-977d-e8c0ef19a9b4)

### c) Doh!

Tein kirjoitusvirheen Testi.txt tiedostossa ja tallensin.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/8d20abcd-3795-4e10-afa6-d83963668ec4)

Lisäsin muutokset seuraavaan tallennukseen ja tuhosin ne

        git add .
        git reset --hard

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/05a6c5e5-fcc5-4f51-bd5f-8b093463bbeb)

Muutokset tuhoutui

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/fbc0b641-dd96-4c89-8f02-0c5de57fc13d)

d) ### Tukki

        git log

Varaston lokissa näkyy aikaisemmat commitit.

Nimeni ja sähköpostiosoitteeni näkyy kuten pitää.

![kuva](https://github.com/simoheinimaki/palvelinten-hallinta/assets/165195779/bb6c747c-e359-402a-883e-8b024d9d4235)




       






###
