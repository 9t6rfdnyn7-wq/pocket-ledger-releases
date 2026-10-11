# pocket-ledger-releases
my finance app

## Pocket-Ledgeri uuendused

Pocket-Ledgeri töölauaäpi paigaldajate ja versiooniinfo avalik hoidla.
Rakenduse lähtekoodi hoitakse eraldi.

Maci ja Windowsi [testversiooni paigaldajad](https://github.com/9t6rfdnyn7-wq/pocket-ledger-releases/releases)
on avalikult saadaval Releases-vaates. `updates.json` sisaldab iga platvormi
viimast kontrollitud paketti; Maci ja Windowsi pakett võivad valmida eri ajal.

Paigaldatud Maci või Windowsi äpp, milles uuenduskanal on seadistatud, kontrollib
versiooni käivitamisel. Uuem versioon või sama versiooni kõrgem
tegelik ehitusnumber pakub nuppu „Ava allalaadimine”. Sama või vanemat
paketti ei pakuta. Paigaldaja allalaadimine ja paigaldamine on käsitsi.
V4.34 ja varasemad äpid vajavad uuenduskanaliga versiooni esmast
käsitsi paigaldamist. Veebäppi uuendatakse selle eraldi veebikanalis.

Maci DMG sisaldab PKG-paigaldajat. Avaldatud pakett on kohalikult
allkirjastatud testpakett; Apple'i notariseerimist selle ehitusega ei tehtud.
Väljalase on GitHubis märgitud Pre-release'iks. Äpp loeb `updates.json`
versiooniinfot, seega GitHubi Pre-release märge ei keela selle uuendusteavitust.

Rakenduse kasutustingimuste ning valmis pakenduse litsentsiteabe
ettevalmistus jätkub. Kaasatud teekide oma litsentsid ja teated säilivad.

## Automaatne avaldamine

Privaatse lähtekoodihoidla main-ehituse töövood saavad kontrollitud DMG ja EXE
siia otse avaldada. Ühekordne seadistus toimub lähtekoodihoidla GitHub Actionsis.
Automaatse väljalaske nimi sisaldab versiooni ja ehitusnumbrit, näiteks
`v4.37-build43701`. Senised käsitsi avaldatud väljalasked säilivad.

Avaldamine kontrollib valmis paketi päritolu ja räsi ning laadib avaliku faili
autentimiseta uuesti alla. Alles seejärel uuendatakse `updates.json` vastavat
platvormi. Teise platvormi kirje säilib. Vanemat versiooni ei pakuta uuema
asemel ning sama versiooni/ehitusnumbri erinevaid baite ei kirjutata üle.
Iga automaatne pakett saab platvormi kontrollsummafaili. Lähtekoodi ega
privaatseid ehitusraporteid siin ei avaldata.
