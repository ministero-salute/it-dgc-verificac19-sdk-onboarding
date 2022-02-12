# Changelog
Tutte le modifiche più importanti effettuate sull'SDK di riferimento 
[Digital Green Certificate SDK Android](https://github.com/ministero-salute/it-dgc-verificac19-sdk-android)
saranno riportate in questo documento, al fine di aiutare gli altri sviluppatori
a rimanere in linea con le modifiche.

## [1.1.5] - 14/02/2022

### Aggiunto

- Modalità **Lavoro** = se la modalità `LAVORO` è attiva, sono considerati validi solo :

- - certificati vaccinali rilasciati a seguito della somministrazione di una dose di richiamo (booster) **(!)**
- - certificati vaccinali rilasciati al completamento del ciclo vaccinale **(!)**
- - certificati di guarigione
- - certificati di esenzione vaccinale
- - certificati di tamponi PCR/RAT negativi & rilasciati a soggetti aventi meno di 50 anni di età

> **(!)** _sulla base del tipo di vaccino o ciclo completato da più di 180gg e fino a 270gg può richiedere la contestuale presentazione di un esito negativo di un test al SARS-CoV-2 eseguito nelle 48 ore precedenti_
<br>

- Modalità **Ingresso IT** = se la modalità `INGRESSO IT` è attiva, sono applicate le regole di validazione europee per la circolazione tra gli Stati Membri, considerando validi :

- - certificati vaccinali rilasciati a seguito della somministrazione di una dose di richiamo (booster)
- - certificati vaccinali rilasciati al completamento del ciclo vaccinale 
- - certificati di guarigione
- - certificati di tamponi PCR/RAT negativi

## [1.1.4] - 04/02/2022

### Aggiunto

- Modalità **Studenti** = se la modalità `STUDENTI` è attiva, sono considerati validi :

- - certificati vaccinali rilasciati a seguito della somministrazione di una dose di richiamo (booster)
- - certificati vaccinali rilasciati al completamento del ciclo vaccinale & emessi da meno di 120 giorni
- - certificati di guarigione emessi da meno di 120 giorni
- - certificati di esenzione vaccinale

## [1.1.3] - 30/01/2022

### Aggiunto

- Supporto alle nuove Medicinal Rules differenziate IT / NOT_IT introdotte in Validation Rules per i valori di start/end dei certificati vaccinali e di guarigione

## [1.1.2] - 22/01/2022

### Aggiunto
- Aggiunto supporto ai certificati di esenzione, [qui](https://github.com/ministero-salute/it-dgc-documentation/blob/master/EXEMPTIONS.md) la documentazione

## [1.1.1] - 27/12/2021

### Aggiunto
- Modalità Booster (se la modalità BOOSTER è attiva allora sono considerati validi solo i certificati vaccinali rilasciati a seguito della somministrazione di una dose di richiamo (booster) e quelli rilasciati al completamento del ciclo vaccinale, richiedendo per questi ultimi una ulteriore validazione di un tampone)

## [1.1.0] - 21/12/2021

### Aggiunto
- Unificati gli stati di `certificato valido`
- DRL (DGC Revocation List, [qui](https://github.com/ministero-salute/it-dgc-documentation/blob/master/DRL.md) la documentazione)

### Rimosso
- Rimosso lo stato `PARTIALLY_VALID`

## [1.0.4] - 02/12/2021
### Aggiunto
- Modalità Super Green Pass (se modalità SGP è attiva allora i test sono sempre non validi)

