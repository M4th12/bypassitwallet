# Guida su come far funzionare IT-Wallet su dispositivi con bootloader sbloccato o con custom rom
⚠️ Attenzione: Questa guida non é certificata che funzioni al 100% su tutti i dispositivi o ROM. ⚠️

Testata su Poco F2 Pro con LineageOS 23.2, funzionante 07/10/2026.

Da giugno Google ha aggiornato il modo in cui viene verificata l'integrità del dispositivo. Dispositivi con Android 13 o superiore potrebbero fallire più facilmente questo fix.

## Requisiti

- Avere **Magisk**, **KernelSU-Next** o **Apatch**

## Moduli necessari

- [Play Integrity Fix Inject](https://github.com/osm0sis/PlayIntegrityFork/releases)
- [ReZygisk](https://github.com/PerformanC/ReZygisk/releases)
- [Specter](https://github.com/dpejoh/specter/releases)

## Opzionali

- [HMA-OSS](https://github.com/frknkrc44/HMA-OSS/releases)


## Passaggi

- Installateli in ordine come qui sopra e poi riavviate. Se avete KSU o Apatch, assicutatevi di aver già installato [ReZygisk](https://github.com/PerformanC/ReZygisk/releases).

- Dopo il riavvio aprite il vostro root manager, nella sezione moduli dove c'è il moduluto Play Integrity Fix cliccate il tasto "Action", vi si aprira' un interfaccia web

<img width="1080" height="1884" alt="image" src="https://github.com/user-attachments/assets/48279c74-b44a-4119-a530-bd83133f5f52" />

- Ora dovrebbe essere tutto funzionante, se tutto ok dovreste vedere questo

<img width="869" height="762" alt="image" src="https://github.com/user-attachments/assets/32297705-f1c0-4bc8-bc22-d915afc949d4" />


## FAQ

- Con il nuovo metodo che Google usa per verificare l'integrità molti telefoni potrebbero non più passare questo fix.

- Per avere le migliori chance controllate che la vostra ROM sia firmata con chiavi private, non abbia nomi di kernel bannati, abbia SeLinux Enforced e che abbia lo storage criptato

