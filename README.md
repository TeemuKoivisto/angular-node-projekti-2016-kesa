# angular-node-projekti-2016-kesa

Säästän tämän repositorion liialta informaatiotulvalta. Eli juuh Angular ja Node, cool. Mitä sit?

Noh tässä on esimerkki pohjani [Angular](https://github.com/TeemuKoivisto/simple-angular-bootstrap) projektiin ja [Node](https://github.com/TeemuKoivisto/simple-node-bootstrap) projektiin. Helpoin tapa kopioida ne itselle on forkkaamalla, toiseksi helpoin on kopiointi ja uuden repon luonti. Kaikki käy.

Jos ne eivät kelpaa, aina voi etsiä omia ratkaisuja tai turvautua vaikkapa Yeomanin [gulp-angular-generaattoriin](https://github.com/Swiip/generator-gulp-angular) tai [Fountainin](https://github.com/FountainJS/generator-fountain-webapp). Omat esimerkkini tein yksinkertaisuutta ajatellen.

## Noden asennus koulun koneelle
HUOM. Jos haluat asentaa Noden koulun koneelle tee ensin normi nvm asennus eli ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.4/install.sh | bash``` ja sitten ```nvm install node``` tai ```nvm install 6.3.1```. Tämän jälkeen sinun pitää mennä kotikansioon eli Homeen ja editoida ```.bashrc``` filua seuraavasti:
```bash
export NVM_DIR="/home/teekoivi/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
```

Muutat muotoon:
```bash
export NVM_DIR="/home/ad/fshome6/u6/t/teekoivi/Linux/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
```

Jossa teekoivin korvaat omalla AD-tunnuksellasi. En kyllä tajua miksi nvm:n asennus on alkanut tuolla tavalla temppuilemaan.

## Heroku
Jos haluat laittaa sovelluksesi [Herokuun](https://www.heroku.com/) suosittelen [Traviksen](https://travis-ci.org) käyttämistä.

1. Eli rekisteröidy molempiin, Travikseen ei tarvitse kuin GitHub tunnukset.
2. Sitten Traviksessa vedä täpät vihreiksi GitHub repositorioille, jotka haluat 'buildata' kun niihin tehdään muutoksia
3. Tämän jälkeen joudut asentamaan [Heroku toolbeltin](https://toolbelt.heroku.com/) jolla kykenet luomaan uusia appeja ja manuaalisesti puskemaan niihin jos tarve vaatii (tai jos et käytä Travista)
4. Jonka jälkeen joudut asentamaan [Travis client gemin](https://github.com/travis-ci/travis.rb#readme), hurraa. Travis gemia et tarvitse kuin luodessasi ```.travis.yml``` tiedostoa joka luodaan kerran per projekti mutta jonka heroku-avaimen kryptaukseen tarvitset gemiä.
5. Ohjeet löytyvät [tästä](https://docs.travis-ci.com/user/deployment/heroku), miten ```yml``` generoidaan. Periaatteessa ensin kirjoitat ```heroku create <app-name>``` johon app-namin korvaat oman sovelluksesi nimellä. Sitten jos muistini pelaa oikein kirjoitat ```travis setup heroku``` jolloin travis luo sinulle kryptatun avaimen ja perus ```yml``` pohjan, johon voit sitten lisätä [Coverallsin](https://coveralls.io/) kuten esimerkkiprojekteissa jos haluat rivikattavuus raportin projektin README:hen. Eli rekisteröidyt Coverallsiin, lisäät täpät kuten Traviksessa, pidät huolen että ```coveralls``` npm-paketti on ```package.json```:issa ja ```.travis.yml``` tiedostossa on rivi ```  - cat ./coverage/report-lcov/lcov.info | coveralls``` aivan kuten esimerkki projektin ```.travis.yml```:ssä

Niillä pitäisi päästä alkuun. Jos ja kun varmaan kysymyksiä tulee, niihin voi löytää vastauksia vanhoista materiaalista, internetistä tai minulta.

## Vanhat kurssisivut
[k2014](https://github.com/tuhoojabotti/AngularJS-ohjelmointiprojekti-k2014)
[s2015](https://github.com/Kaltsoon/AngularJS-ja-NodeJS-ohjelmointiprojekti-s2015)

## Palautus

Muistakaa tuntikirjanpito jokaiselta päivältä jolloin teitte töitä! Ja jos on ryhmätyö niin molemmilla on omansa.

[Kurssipalautus Google-formin kautta.](https://docs.google.com/forms/u/0/d/e/1FAIpQLSfndBvApdQ4rBrUWSBvussd_ICep5n5ithcslduQ31VSj8Cog/viewform)
