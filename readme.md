# Docker Internals: Namespaces e CGroups Spiegati

Guida completa ai meccanismi interni di Docker e all'isolamento dei container tramite **Linux namespaces** e **cgroups**. Include spiegazioni dettagliate, esempi pratici e demo da eseguire sul proprio sistema.

## Contenuti

- Introduzione a Docker e containerizzazione
- Differenze tra container e macchine virtuali
- Architettura interna di Docker
- Isolamento tramite Linux Namespaces:
  - PID Namespace
  - Network Namespace
  - Altri namespace supportati
- Controllo delle risorse con CGroups:
  - Limitazione CPU, memoria, I/O e rete
  - Interfaccia `/sys/fs/cgroup/`
- Demo pratiche:
  - Isolamento dei processi con PID namespace
  - Port mapping e isolamento di rete
  - Limitazione memoria e CPU via cgroups
  - Monitoraggio real-time delle risorse

## Esecuzione delle demo

Le demo possono essere eseguite direttamente su un sistema Linux con Docker installato. Alcune richiedono i seguenti strumenti aggiuntivi:

- `nsenter` (pacchetto `util-linux`)
- `stress` (installabile nel container tramite `apt`)
- `dmesg`, `ps`, `pstree`, `watch`

Tutti i comandi sono testati su distribuzioni basate su Debian (es. Ubuntu).

## Immagini

Le immagini incluse illustrano:

- Architettura di Docker
- Differenze tra container e VM
- Gerarchia dei PID namespace
- Isolamento di rete tra container

Assicurati di posizionare le immagini nella cartella `./imgs/` come indicato nel post.

## Licenza

Contenuti rilasciati sotto licenza MIT, tranne dove diversamente specificato.  
Autore: Francesco Montelli  
[Blog post completo](https://montelli.dev/posts/docker-internals/) 
