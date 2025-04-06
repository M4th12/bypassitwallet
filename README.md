# Questa é una guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom
- Aggiornamento, potrebbere esserci un [problema con l'app iO di base](https://www.dday.it/redazione/51379/app-io-e-android-i-documenti-sullo-smartphone-non-vanno-nemmeno-con-alcuni-dispositivi-sicuri-ecco-perche), aspettiamo i prossimi aggiornamenti
- Secndo aggiornamento, l'app iO sembra che controlli anche se nelle specifiche del telefono trova parole come Lineage in più sembra che abbia un meccanismo nuovo simile a Revolut per rilevare la presenza di root che per il momento sembra non ci sia una soluzione, se in futuro si aprirà una soluzione la guida verrà aggiornata
## Requisiti

- Avere **Magisk installato** e anche **Zygisk** abilitato.

- Avere una keybox, bisogna che vi procurate un file keybox.xml. Altrimenti scaricate [questa](video/Chiavescatola.zip)


## Moduli necessari

- [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/releases)
- [Shamiko](https://github.com/LSPosed/LSPosed.github.io/releases/)
- [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases)
- [Tricky Store Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/tag/v3.7)
- [KSU Web UI](https://github.com/5ec1cff/KsuWebUIStandalone/releases/tag/v1.0)

## Steps

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate.

- Aprite KSU Web UI e da li selezionate Play Store, Play Services e l'app iO

- Se dopo aver installato Magisk alcune app rilevano che avete il root andate in [Impostazioni > Configura Lista Blocco](video/blocklist.mp4) e spuntate tutte le app che lo rilevano, sopratutto Google Play Service e anche iO
  
- Ora dovrebbe essere tutto funzionante

(Per vedere se effettivamente ha funzionato scaricate [KeyAttestation](https://github.com/vvb2060/KeyAttestation/releases) e se tutto è corretto dovreste vedere [questo](video/ok.png))

## FAQ

- Per [abilitare Zygisk](video/zygisk.mp4) basta andare nelle Impostazioni di Magisk e attivare l'opzione

