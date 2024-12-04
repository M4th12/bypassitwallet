# Questa é una guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom

## Requisiti

- Avere **Magisk installato** e anche **Zygisk** abilitato.

- Avere una keybox (anche giá bannata), bisogna che vi procurate un file keybox.xml. Altrimenti scaricate [questa](video/Chiavescatola.zip)


## Steps

- Prima di tutto scaricare i moduli necessari [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases), [Shamiko](https://github.com/LSPosed/LSPosed.github.io/releases/) opzionale anche [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/releases).

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate.

- Dopo il riavvio, tramite un file manager con accesso root, io uso [FX](https://play.google.com/store/apps/details?id=nextapp.fx&hl=it) andate nella seguente directory

- [data/adb/tricky_store/](video/fxrootetrickystore.mp4)

- All'interno dovete incollare il file **keybox.xml**

- Dopodiche andate nel file **target.txt** e metterci dentro il nome del pacchetto dell'app iO. **it.pagopa.io.app**

- Ora dovrebbe essere tutto funzionante

(Per vedere se effettivamente ha funzionato scaricate [KeyAttestation](https://github.com/vvb2060/KeyAttestation/releases) é se tutto e corretto dovreste vedere [questo](video/ok.png))

## FAQ

- Per [avere accesso root con FX](video/fxrootetrickystore.mp4) basta andare nelle Impostazioni, scorrere fino a Developer/Root e ablilitare l'opzione

- Per [abilitare Zygisk](video/zygisk.mp4) basta andare nelle Impostazioni di Magisk e attivare l'opzione

- Se dopo aver installato Magisk alcune app rilevano che avete il root andate in [Impostazioni > Configura Lista Blocco](video/blocklist.mp4) e spuntate tutte le app che lo rilevano, sopratutto Google Play Services
