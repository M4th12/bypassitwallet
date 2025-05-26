# Guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom
⚠️ Attenzione: Questa guida non é certificata che funzioni al 100% su tutti i dispositivi o Custom ROM. ⚠️

Testata su un Mi A3 con crDroid (A15), ancora funzionante 21/05/2025.

Da questo mese Google ha aggiornato il modo in cui viene verificata l'integrità del dispositivo. Dispositivi con Android 13 o superiore potrebbero fallire più facilmente questo fix.

## Requisiti

- Avere **Magisk installato** (versione 29 o superiore in quanto viene rilevata con più difficoltà) e anche **Zygisk** abilitato o **KSU** con **Zygisk-Next** installato

## Moduli necessari

- [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/releases)
- [Shamiko](https://github.com/LSPosed/LSPosed.github.io/releases/)
- [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases)
- [Tricky Store Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/)
- [KSU Web UI](https://github.com/5ec1cff/KsuWebUIStandalone/releases/) (Serve solo per chi ha Magisk)

## Steps

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate. Se avete KSU, assicutatevi di aver già installato Zygisk-Next.

- Dopo il riavvio aprite Magisk, nella sezione moduli dove c'è il moduluto Play Integrity Fix cliccate il tasto "Action". Per KSU invece cliccate il tasto per aprire la WebUI del modulo e fate "Fetch new pif"

- Aprite KSU Web UI e cliccate Tricky Store (da KSU basta fare come per Play Integrity Fix), da li selezionate Play Store, Play Services e l'app iO (Anche l'app KeyAttestation se volete verificare se il bootloader risulta bloccato)

- Dopo cliccate sul menu hamburger e selezionate "Imposta keybox Valida", sempre da quel menù cliccate anche "Imposta patch di sicurezza", dopo premete "Ottieni data patch di sicurezza" e poi salva. [video](video/tricky.mp4)

- Se alcune app rilevano Magisk andate in [Impostazioni > Configura Lista Blocco](video/blocklist.mp4) e spuntate tutte le app che lo rilevano, soprattutto Google Play Service, Play Store e iO
  
- Ora dovrebbe essere tutto funzionante

(Per vedere se effettivamente ha funzionato scaricate [KeyAttestation](https://github.com/vvb2060/KeyAttestation/releases) e se tutto è corretto dovreste vedere [questo](video/ok.png))

## FAQ

- Per [abilitare Zygisk](video/zygisk.mp4) basta andare nelle Impostazioni di Magisk e attivare l'opzione

- KSU Web UI per funzionare ha bisogno dell'accesso root, nel caso ve lo chieda concedeteli l'accesso

- Se più avanti notate che non riuscite più ad ottenere l'integrità. Rifate il passaggio 2 e 4. Nel caso del 4 controllate se vi propone degli aggiornamenti e fateli

- Con il nuovo metodo che Google usa per verificare l'integrità molti telefoni potrebbero non più passare questo fix.

- Per avere le migliori chance controllate che la vostra ROM sia firmata con chiavi private, non abbia nomi di kernel bannati, abbia SeLinux Enforced e che abbia la Crifratura funzionante

