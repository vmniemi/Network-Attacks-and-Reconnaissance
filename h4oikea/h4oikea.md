Kotitehtävä:

# 1. Tarkastele käytössäsi olevia RFID tuotteita, mieti miten hyvin olet suojautunut RFID urkinnalta?

Minulla on vain RFID-tuotteista käytössä pankkikortti, pankkikortissa lukuetäisyys on muutama senttimetri joten uskoisin että se pysyy melko turvassa.

Toki voisin hankkia sellaisen RFID-blocking kortin lompakkoon, jos haluaisin extra suojaa
   
# 2. Tutustu APDU komentojen rakenteeseen (voit käyttää tekoälyä tutustumiseen)


APDU on kahta erilaista: command ja response. RFID lukija lähettää commandin ja RFID-laite esim. kortti lähettää responsen.


Command rakenne, neljä ensimmäistä bittiä on pakollista, loppuun voi lisätä lisätietoja

Pakolliset

CLA:	Mikä kanava, mitä standardeja käyttää(käyttääkö ISOn: vai yrityksen omaa)
INS:	Ohjekoodi, mitä halutaan luetulta kortilta
P1	ja P2: parametrit, esim. mihin tiedostoon tieto kirjataan

Valinnaiset kentät


Lc:		Datan pituus
Data:  tietosisältö(payload), jos haluaa erikseen spesifioida
Le:	Odotetun vastauksen pituus



Response rakenne


Response data: Tieto joka tulee kortilta takaisin

SW1 ja SW2: Status koodi esim. 90 00 tarkoittaa, että tapahtuma onnistui.



   
# 3. Tutki ja kerro minkä mielenkiintoisen RFID hakkerointi uutiset löysit. (Vinkki, useimmat liittyvät henkilökortteihin)


https://yaledailynews.com/blog/2025/04/03/yale-police-arrest-suspect-for-attempted-berkeley-burglary/

Uutisessa poliisi pidätti henkilön, joka yritti päästä sisään Berkeley Collegeen kloonatulla henkilökortilla. Kyseinen henkilö saatiin kiinni, koska hän käytti samaa korttia useilla sisäänkäynneillä ja poliisi tunnisti henkilön aikaisemmasta murtovarkaudesta tuntomerkkien perusteella. Artikkelissa mainitaan, että koulussa käytetyissä henkilökorteissa on uniikki tunnistenumero, mutta se on staattinen eli ei koskaan muutu, niin nämä kortit ovat haavoittuvaisia hyökkäyksiin, jossa käytetään kloonattuja kortteja. Tämä pidätys voi johtaa turvaprotokollien tarkistamiseen tai tiukentamiseen rakennuksissa, jotka ovat riippuvaisia ​​​​henkilöllisyyteen perustuvasta kulunvalvonnasta. 





## Lähteet

https://en.wikipedia.org/wiki/Smart_card_application_protocol_data_unit


https://yaledailynews.com/blog/2025/04/03/yale-police-arrest-suspect-for-attempted-berkeley-burglary/

