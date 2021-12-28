# Changelog
Tutte le modifiche più importanti effettuate sull'SDK di riferimento 
[Digital Green Certificate SDK Android](https://github.com/ministero-salute/it-dgc-verificac19-sdk-android)
saranno riportate in questo documento, al fine di aiutare gli altri sviluppatori
a rimanere in linea con le modifiche.

## [1.1.1] - 27/12/2021

### Aggiunto
- Modalità Booster (se modalità BOOSTER è attiva allora sono considerati validi solo i certificati vaccinali a seguito di dose richiamo/booster e quelli di completamento del ciclo vaccinale, richiedendo per questi ultimi ulteriore validazione di un test)

## [1.1.0] - 21/12/2021

### Aggiunto
- Unificati gli stati di `certificato valido`
- DRL (DGC Revocation List, [qui](https://github.com/ministero-salute/it-dgc-documentation/blob/master/DRL.md) la documentazione)

### Rimosso
- Rimosso lo stato `PARTIALLY_VALID`

## [1.0.4] - 02/12/2021
### Aggiunto
- Modalità Super Green Pass (se modalità SGP è attiva allora i test sono sempre non validi)

