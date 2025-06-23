# Guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom
⚠️ Attenzione: Questa guida non é certificata che funzioni al 100% su tutti i dispositivi o Custom ROM. ⚠️

Testata su un Mi A3 con crDroid (A15), ancora funzionante 23/06/2025.

Da questo mese Google ha aggiornato il modo in cui viene verificata l'integrità del dispositivo. Dispositivi con Android 13 o superiore potrebbero fallire più facilmente questo fix.

## Requisiti

- Avere **Magisk installato** (versione 29 o superiore in quanto viene rilevata con più difficoltà) e anche **Zygisk** abilitato o **KSU** con **ReZygisk o Zygisk-Next** installato

## Moduli necessari

- [Play Integrity Fork](https://github.com/osm0sis/PlayIntegrityFork/releases)
- [NoHello](https://github.com/MhmRdd/NoHello/releases)
- [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases)
- [Tricky Store Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/)
- [KSU Web UI](https://github.com/5ec1cff/KsuWebUIStandalone/releases/) (Serve solo per chi ha Magisk)

## Steps

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate. Se avete KSU, assicutatevi di aver già installato [ReZygisk](https://github.com/PerformanC/ReZygisk/releases).

- Dopo il riavvio aprite Magisk, nella sezione moduli dove c'è il moduluto Play Integrity Fork cliccate il tasto "Action", stessa cosa anche per KSU
  
	- **Questo passaggio é solo per chi ha Android 13 o superiore**, se non avete queste versioni saltate questo passaggio o potete tentare ma molto probabilmete non riuscirete ad ottenere tutte le spunte.
   
	- ⚠️ AVVISO il PlayStore con questa modifica sará quasi inutilizzabile (per il momento) come alternativa potete usare [Aurora Store](https://f-droid.org/it/packages/com.aurora.store/) ⚠️
  - Dopo aver premuto il tasto Action bisogna dirigersi nella cartella /data/adb/modules/playintegrityfix e cercare il file custom.pif.json
  - Aprite il file e nella sezione Advanced Setting aggiungete "spoofVendingSdk": "1", (Ricordatevi la , alla fine), salvate e riavviate il telefono
    

- Aprite KSU Web UI e cliccate Tricky Store (da KSU identico), da li selezionate Play Store, Play Services e l'app iO (Anche l'app KeyAttestation se volete verificare se il bootloader risulta bloccato)

- Dopo cliccate sul menu hamburger e selezionate "Imposta keybox Valida". [video](video/tricky.mp4)

- Se alcune app rilevano Magisk andate in [Impostazioni > Configura Lista Blocco](video/blocklist.mp4) e spuntate tutte le app che lo rilevano, soprattutto Google Play Service, Play Store e iO. Su KSU assicuratevi di aver attivato l'opzione "Scollega moduli di default".
  
- Ora dovrebbe essere tutto funzionante

(Per vedere se effettivamente ha funzionato scaricate [KeyAttestation](https://github.com/vvb2060/KeyAttestation/releases) e se tutto è corretto dovreste vedere [questo](video/ok.png))

## FAQ

- Per [abilitare Zygisk](video/zygisk.mp4) basta andare nelle Impostazioni di Magisk e attivare l'opzione

- KSU Web UI per funzionare ha bisogno dell'accesso root, nel caso ve lo chieda concedeteli l'accesso

- Se più avanti notate che non riuscite più ad ottenere l'integrità. Rifate il passaggio 2 e 4. Nel caso del 4 controllate se vi propone degli aggiornamenti e fateli

- Con il nuovo metodo che Google usa per verificare l'integrità molti telefoni potrebbero non più passare questo fix.

- Per avere le migliori chance controllate che la vostra ROM sia firmata con chiavi private, non abbia nomi di kernel bannati, abbia SeLinux Enforced e che abbia lo storage criptato

