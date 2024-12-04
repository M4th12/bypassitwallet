# Questa é una guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom

## Requisiti

- Avere **Magisk installato** e anche **Zygisk** abilitato.

- Avere una keybox (anche giá bannata)


## Steps

- Prima di tutto scaricare i moduli necessari [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases), [Shamiko](https://github.com/LSPosed/LSPosed.github.io/releases/) opzionale anche [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/releases).

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate.

- Dopo il riavvio, tramite un file manager con accesso root, io uso [FX](https://play.google.com/store/apps/details?id=nextapp.fx&hl=it) andate nella seguente directory

- data/adb/tricky_store/

- All'interno dovete incollare il file **keybox.xml**

- Dopodiche andate nel file **target.txt** e metterci dentro il nome del pacchetto dell'app iO. **it.pagopa.io.app**

- Ora dovrebbe essere tutto funzionante
