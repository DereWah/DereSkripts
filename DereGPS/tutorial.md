# Come aggiungere DereGPS alla vostra ResourcePack

In questo piccolo tutorial vi mostrerò come potete impostare la vostra resource pack in modo che mostri le icone di DereGPS. Questo tutorial si divide in 3 casi:

- Non hai una resource pack custom sul tuo server

- Hai una resource pack custom sul tuo server ma non usi i custom fonts (icone custom)

- Hai una resource pack custom sul tuo server e usi i custom fonts.

## Non hai una resource pack custom sul tuo server

In questo caso è semplicissimo aggiungere il pacchetto di risorse: scaricalo a questo link e aggiungilo ai pacchetti del tuo server. Così facendo i players lo scaricheranno in automatico e vedranno l'icona del GPS completamente funzionante.

## Hai una resource pack custom sul tuo server ma non usi i custom fonts (icone custom)

Se il tuo server non usa icone custom, allora è semplice modificare il tuo resource pack "mixandolo" con quello di DereGPS. Scarica il pack da questo link, e sposta tutte le cartelle da `DereGPS\assets\minecraft` al tuo resource pack, nello stesso percorso. Assicurati di mettere tutti i files nel loro posto, così che il resource pack funzioni!

Per assicurarti che tutto sia andato a buon fine, controlla che:

- Esista la cartella `\assets\minecraft\textures\custom` e che abbia al suo interno tutte le direzioni del GPS. 
- Il file `\assets\minecraft\lang\en_us.json` contenga tanti caratteri come  `"offset.90": "\uF82B\uF829\uF828\uF822%s\uF80B\uF809\uF808\uF802"`
- Il file `\assets\minecraft\font\default.json` contenga una sorta di config con tutti i caratteri, con i percorsi specifici ad ogni icona del dereGPS.

Adesso ti basta impostare il pack come pacchetto di default per il server ed i tuoi players saranno in grado di vedere l'icona del DereGPS!

## Hai una resource pack custom sul tuo server e usi i custom fonts.

Se hai una resource pack che usa custom fonts, suppongo tu sia in grado di comprendere come funzionano e cosa sono. Se non lo sei, fai eseguire il setup al membro dello staff che si è occupato di impostarli per te.

Come prima cosa segui tutti gli step della sezione sopra, MA NON sovrascrivere il file `\assets\minecraft\font\default.json`. Li stanno le tue icone custom pre-esistenti, e sovrascrivendolo perderai il config.

Adesso apri il file `\assets\minecraft\font\default.json`, e tra le custom icons che hai già presenti, assicurati che nessuna di esse usi i caratteri tra E170,E171,E172,E173, ... , E178

Per vederlo basta che nessuno di questi caratteri compaia nella voce "chars" delle tue custom icons già esistenti.

### Se non sono già occupati

Prendi il file default.json del pack DereGPS e copia e incolla tutte le nuove icone nel tuo default.json. **ASSICURATI DI RISPETTARE LE REGOLE DI JSON**! Metti le virgole tra ciascuna voce e tra ciascuna sezione.

Dopodiché il pack sarà pronto all'uso.

### Se sono già occupati

Puoi scegliere o di cambiare le tue icone già esistenti, assegnando loro nuovi caratteri, o invece di cambiare quelle di DereGPS. Qui ti spiegherò come cambiare quelle di DereGPS:

Vai su questo sito: https://unicodes.jessetane.com/ ed in basso a destra seleziona "Private Use Area"

Scegli  dei "quadratini" e cliccaci sopra, assicurandoti poi che non siano caratteri unicode ancora già usati dal tuo pack.

Copia il quadratino (proprio il carattere) e ricordati anche il suo unicode associato (Per esempio E0F8 = )

Apri lo skript DereGPS.sk e incolla il quadratino nelle options in cima allo skript. Accanto aggiorna anche il commento, aggiornandolo con il nuovo valore.

Poi apri il default.json, e crea/copia dal vecchio default.json di DereGPS una nuova sezione, e aggiornala come qui sotto:

```		{
            "type": "bitmap",
            "file": "minecraft:custom/<DIREZIONE DELLA FRECCIA>.png",
            "ascent": 9,
            "height": 9,
            "chars": ["\u<ID UNICODE SALVATO>"]
        },
```

Per capire cosa inserire in <DIREZIONE DELLA FRECCIA>, segui la tabella qui sotto:

|Option in DereGPS.sk|Nome file da inserire in default.json|
| ------------ | ------------ |
|gps_forward|gpsf.png|
|gps_forwardleft   |gpsfl.png   |
|gps_left   |gpsl.png   |
|gps_backwardsleft   |gpsbl.png   |
|gps_backwards   |gpsb.png   |
|gps_backwardsright   |gpsbr.png   |
|gps_right   |gpsr.png   |
|gps_forwardright   |gpsfr.png   |
|gps_icon   |gpsf.png   |

Non è difficile intuire comunque che la direzione della option viene abbreviata nel nome file soltanto con la iniziale.

Dopodiché tutto sarà pronto all'uso e potrai aggiungere il pack nel server!

# Possibili problemi

Se riscontri problemi, apri pure un issue riguardando l'sk su github: https://github.com/DereWah/DereSkripts/issues

Oppure contattami su telegram: https://t.me/DereWah


