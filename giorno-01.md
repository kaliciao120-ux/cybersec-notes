# Giorno 1: Come funziona Internet

Data: 17/11/2026

## Argomenti
- IP, DNS e HTTP
- Prove pratiche con ping, nslookup e curl

## Comandi 

### ping
`ping -c 4 google.com` invia 4 pacchetti. Senza `-c` su Linux va all'infinito (si ferma con Ctrl+C).

### nslookup
`nslookup google.com` ha restituito 1 indirizzo IPv4 (record A) e 4 IPv6 (record AAAA).
Il resolver DNS era un IP privato (10.x.x.x) e la risposta era "non-authoritative".

### curl
`curl -I https://google.com` ha restituito **301 Moved Permanently** con redirect verso https://www.google.com/.
Header notati: server, x-frame-options, content-security-policy-report-only.

## Argomenti imparati
- un IP è come il propio indirizzo di casa e serve per poter mandare un pacchetto dati ad un utente/server specifico
- il DNS è come una specie di traduttore che trasforma il nome del sito che cerchi nel indirizzo IP di quel sito
- HTTP sta per HyperText Transfer Protocol, regola la comunicazione sul web attraverso un modello richiesta-risposta
- Un 301 è un redirect permanente: il server mi dice di andare a un altro indirizzo
