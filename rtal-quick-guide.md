# Guida rapida all'utilizzo di rtal
**N.B:** ad oggi per fare login sul sistema è necessario scaricare rtal versione 0.2.0 perché altre versioni non permettono l'autenticazione verso il server.

- Per installare rtal:
```sh
mkdir -p ~/.local/bin && cd ~/.local/bin && wget https://github.com/Guilucand/rtal-algo-client/releases/download/V1.0.1/rtal-x86_64-unknown-linux-gnu.tar.gz && tar -xf rtal-x86_64-unknown-linux-gnu.tar.gz && rm rtal-x86_64-unknown-linux-gnu.tar.gz && chmod +x rtal && cd ~
```
- Per disinstallare rtal
```sh
rm ~/.local/bin/rtal
```

La lista dei server è:
- algo
- esercizi
- esame
da anteporre al link ad esempio ``wss://ta.di.univr.it/*nome_server*``
- Login su rtal
``` sh
rtal -s wss://ta.di.univr.it/algo login
```

- Lista dei problemi
``` sh
rtal -s wss://ta.di.univr.it/algo list
```

- Scarica un problema dal server

```sh
rtal -s wss://ta.di.univr.it/algo get *problema*
```

- Scarica scoreboard dal server

```sh
rtal -s wss://ta.di.univr.it/algo get scoreboard
```
- Estrai un archivio **.tar**
```sh
tar -xf nome_archivio.tar
```
- Sottometti una soluzione
```sh
rtal -s wss://ta.di.univr.it/algo connect [nome problema] [-a size=dimensione problema] -f source=[sorgente] -- [lancia binario come ./a.out o python3 sorgente.py]
```

- Utilizza synopsis

```sh
rtal -s wss://ta.di.univr.it/algo connect [nome problema] -f source=[sorgente]
```
