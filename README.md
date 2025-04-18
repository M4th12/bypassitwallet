# Questa é una guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom
⚠️ Attenzione: Questa guida non é certificata che funzioni al 100% su tutti i dispositivi o Custom ROM. ⚠️
## Requisiti

- Avere **Magisk installato** e anche **Zygisk** abilitato o **KSU** con **Zygisk-Next** installato

## Moduli necessari

- [Play Integrity Fix](https://github.com/chiteroman/PlayIntegrityFix/releases)
- [Shamiko](https://github.com/LSPosed/LSPosed.github.io/releases/)
- [Tricky Store](https://github.com/5ec1cff/TrickyStore/releases)
- [Tricky Store Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/tag/v3.7)
- [KSU Web UI](https://github.com/5ec1cff/KsuWebUIStandalone/releases/tag/v1.0) (Serve solo per chi ha Magisk)

## Steps

- Installateli in Magisk come messi in ordine qui sopra e poi riavviate.

- Aprite KSU Web UI e cliccate Tricky Store, da li selezionate Play Store, Play Services e l'app iO (Anche l'app KeyAttestation se volete verificare se la procedura ha funzionato)

- Dopo cliccate sul menu hamburger e selezionate "Imposta keybox Valida" e dopo "Imposta patch di sicurezza", nel menu che vi si aprirá premete "Ottieni data patch di sicurezza" e poi salva. [video](video/tricky.mp4)

- Se dopo aver installato Magisk alcune app rilevano che avete il root andate in [Impostazioni > Configura Lista Blocco](video/blocklist.mp4) e spuntate tutte le app che lo rilevano, sopratutto Google Play Service e anche iO
  
- Ora dovrebbe essere tutto funzionante

(Per vedere se effettivamente ha funzionato scaricate [KeyAttestation](https://github.com/vvb2060/KeyAttestation/releases) e se tutto è corretto dovreste vedere [questo](video/ok.png))

## FAQ

- Per [abilitare Zygisk](video/zygisk.mp4) basta andare nelle Impostazioni di Magisk e attivare l'opzione

- KSU Web UI per funzionare ha bisogno dell'accesso root, nel caso ve lo chieda concedeteli l'accesso

