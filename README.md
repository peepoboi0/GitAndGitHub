# GitAndGitHub

![alt text](githublogo.png)


### Mitä on versiohallinta? 


Versionhallinta on menetelmä, joka auttaa säilömään tietoa ja erilaisia muutoksia, joita siihen on tehty. 

Syyt versionhallintaan:

- Tiedon varmuuskopiointi. Varmuuskopiot sisältävät aikaisemmat ja nykyisen tilan.
- Mahdollistaa tiedon jakamisen, sekä ryhmäprojektien helppouden.


### Mikä on Git?


Git on versionhallinta menetelmä, joka ottaa "kuvan" nykyisestä tiedoston tilasta ja tallentaa tämän snapshotiksi.


### Mikä on GitHub?


GitHub on palvelu, joka mahdollistaa tiedon jakamisen muille samojen tietojen parissa työskenteleville henkilöille. GitHubissa voi myös pitää Git-muotoisia varastoja *(Repository)*.

GitHub toimii myös paikkana, jonne varmuuskopioida tiedostot. 

---


### Git:in käyttö


Git koostuu järjestelmänä kolmesta osasta:

1. Työkansio *(working directory)*
2. Git indeksi *(staging area)*
3. Paikallinen versionhallinta repositorio .git hakemistossa *(local .git)*


### Git:in kanssa työskentely:


**Git:in käyttöönotto:**

Ensimmäisenä käytetään komentoa halutussa työkansiossa: `git init`

Tämän jälkeen määritetään käyttäjänimi: `git config user.name "Etunimi Sukunimi"`

Määritetään sähköpostiosoite: `git config --global user.email "abc.defg@esimerkki.com"`

Katsotaan tallennetut tiedot: `git config --list --global`


**Git:in peruskomentoja:**

Tietoa lisätään Git:in indeksiin komennolla: `git add <tiedosto>`

Tiedon *committaaminen* indeksistä: `git commit -m "viesti"`

Commit listaaminen: `git log` tai `git log --oneline`

Git tilan katsominen: `git status`


### Kuinka tieto menee Git:in ja Github:in välillä

Kun halutaan kytkeä paikallinen työtiedosto GitHub repositorioon:

´git remote add origin https:/github.com/GitHubTunnus/GitHubRepositorio.git`

Tämän jälkeen kytkeminen vahvistetaan komennolla:

`git remote -v`

Sitten työnnetään työkansion tiedot GitHubiin:

`git push -u origin master`


Jos halutaan synkronoida tietoja GitHubista paikalliseen työkansioon:

`git fetch`

Tietojen lataaminen GitHubista paikalliseen työtiedostoon:

`git pull`



### Mikä on branch?

Branch eli Git haara on ominaisuus, joka mahdollistaa haarassa olevien tietojen muuttamisen, ilman että muutokset vaikuttavat työkansion muihin tiedostoihin.

**Komentoja:**

`git branch` - listaa haarat
`git branch haaran_nimi` - lisää haaran
`git merge haaran_nimi` - yhdistää haaran main/master päähaaraan
`git branch -d uusibranch` - poistaa haaran

