# Changelog
Tutte le modifiche più importanti effettuate sull'SDK di riferimento 
[Digital Green Certificate SDK Android](https://github.com/ministero-salute/it-dgc-verificac19-sdk-android)
saranno riportate in questo documento, al fine di aiutare gli altri sviluppatori
a rimanere in linea con le modifiche.

## [1.1.10] - 13/06/2022

### Aggiunto

- Rimozione della modalità Ingresso IT

## [1.1.9] - 19/04/2022

### Aggiunto

- Nuovi Certificati LEAF+BACKUP per SSL pinning. Commit di riferimento [qui](https://github.com/ministero-salute/it-dgc-verificac19-sdk-android/commit/4742dc61e70ea5d26d404e280e725c2becc45cfb)
 
## [1.1.8] - 05/04/2022

### Aggiunto

- Nuova modalità di ingresso IT con regole per ingresso a utenti di età inferiore ai 18 anni. Commit di riferimento [qui](https://github.com/ministero-salute/it-dgc-verificac19-sdk-android/commit/93e3b64e1d5016f0887b1a153147b35a51d06954)
- Rimozione delle modalità Lavoro e Studenti

## [1.1.7] - 30/03/2022

### Aggiunto

- Aggiunto custom header nelle richieste

### Risolto

- Fix su certificato CBIS

## [1.1.6] - 08/03/2022

### Aggiunto

- Recupero di opzioni + descrizioni scanmode da [Validation Rules](https://get.dgc.gov.it/v1/dgc/settings)
- Predisposizione flusso DOUBLE_SCAN per verifiche TEST_NEEDED 


## [1.1.5] - 14/02/2022

### Aggiunto

- Modalità **Lavoro** = se la modalità `LAVORO` è attiva, la validazione dei certificati di vaccinazione/guarigione/tampone & esenzione avviene secondo le regole di :

- - modalità `BASE` (3G) quando intestatario ha meno di 50 anni di età
- - modalità `RAFFORZATA` (2G) quando intestatario ha già compiuto i 50 anni di età **(!)**

> **(!)** _sulla base del tipo di vaccino (autorizzato EMA o meno) o ciclo completato da più di 180gg e fino a 270gg le validazioni in modalità `RAFFORZATA` (2G) possono richiedere la contestuale presentazione di un esito negativo di un test al SARS-CoV-2 eseguito nelle 48 ore precedenti_
<br>

- Modalità **Ingresso IT** = se la modalità `INGRESSO IT` è attiva, sono applicate le regole di validazione europee per la circolazione tra gli Stati Membri.
- Riviste regole secondo l’ultimo Decreto Legge
- Nuove regole vaccini NON IT

## [1.1.4] - 04/02/2022

### Aggiunto

- Modalità **Studenti** = se la modalità `STUDENTI` è attiva, sono considerati validi solo :

- - certificati vaccinali rilasciati a seguito della somministrazione di una dose di richiamo (booster)
- - certificati vaccinali rilasciati al completamento del ciclo vaccinale & emessi da meno di 120 giorni
- - certificati di guarigione emessi da meno di 120 giorni
- - certificati di esenzione vaccinale

> **(!)** _Questa modalità prevede il solo utilizzo dell'app Verifica C19, pertanto non deve essere implementata all'interno degli SDK_

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

