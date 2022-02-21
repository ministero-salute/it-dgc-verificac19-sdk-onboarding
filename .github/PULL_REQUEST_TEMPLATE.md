## Descrizione

<!--- Describe in detail the proposed mods -->

Cosa porta questa PR: ...

<!--- Se non si propone un nuovo SDK è possibile rimuovere il contenuto qua sotto -->
<!--- Mettere una `x` su ogni requisito rispettato dall'SDK: -->

### Repository
- [ ] La licenza è una tra [quelle approvate da OSI](https://opensource.org/licenses) 
- [ ] C'è un README e una documentazione chiara per il funzionamento, l'installazione e l'integrazione

### Funzionamento generico
- [ ] I dati dei Digital Covid Certificate (DCC) non vengono salvati 
- [ ] Non ci sono trasmissioni in rete delle informazioni dei DCC
- [ ] La verifica della validità dei DCC è offline

### Certificati di firma (DSC)
- [ ] C'è una funzione che scarica i DSC da https://get.dgc.gov.it/v1/dgc/signercertificate/update e https://get.dgc.gov.it/v1/dgc/signercertificate/status
- [ ] C'è una funzione di controllo della freschezza dei DSC scaricati (massimo 24 ore)
- [ ] Verifica corretta di una firma dato il suo DSC

### Settings
- [ ] C'è una funzione che scarica i settings (https://get.dgc.gov.it/v1/dgc/settings)
- [ ] C'è una funzione di controllo della freschezza dei settings scaricati (massimo 24 ore)
- [ ] La verifica della validità del DCC applica le regole sanitarie date dai settings
- [ ] La verifica della validità del DCC applica la blacklist in `black_list_uvci`

### Certificate Revocation List (CRL)
- [ ] C'è una funzione che [scarica la CRL e gestisce il resume dello scaricamento](https://github.com/ministero-salute/it-dgc-documentation/blob/master/DRL.md#documentazione)
- [ ] Il setup e l'attivazione della CRL (es. metodi, database locale di supporto, ecc.) sono documentati

### Verifica
- [ ] Esistenza della verifica dei test (tempi dei test e tipologie dei test)
- [ ] Esistenza della verifica della vaccinazione (tempi di vaccinazione e tipologie dei vaccini)
- [ ] Esistenza della verifica in caso di guarigione e check sui tempi
- [ ] Gestisce i vaccini EMA/Non EMA compreso il caso speciale San Marino (Sputnik-V valido solo nel caso di vaccinazione a San Marino)
- [ ] Esistenza della verifica in modalità "Super Green Pass"
- [ ] Esistenza della verifica in modalità Visitatori RSA (ex Booster)
- [ ] Esistenza della verifica in modalità Lavoro
- [ ] Esistenza della verifica in modalità Ingresso in Italia

### Dati malformati
- [ ] Rifiuta Base45 con encoding errato ([testcase](https://github.com/eu-digital-green-certificates/dgc-testdata/blob/main/common/2DCode/raw/B1.json))
- [ ] Rifiuta DGC non corretti ([testcase](https://github.com/eu-digital-green-certificates/dgc-testdata/blob/main/common/2DCode/raw/DGC1.json))

### Validità
Il risultato della verifica di validità è uno di questi possibili stati:

- [ ] `VALID` (il DCC è valido)
- [ ] `TEST_NEEDED` (nella modalità di verifica "Visitatori RSA", si necessita di test)
- [ ] `NOT_VALID_YET` (il certificato non è ancora valido)
- [ ] `NOT_VALID` (il certificato non è valido)
- [ ] `REVOKED` (il certificato è stato revocato)
- [ ] `NOT_EU_DCC` (il certificato non è un EU DCC valido)

<!--- Il repository https://github.com/eu-digital-green-certificates/dgc-testdata ha testcase utili per controllare la correttezza delle librerie -->
