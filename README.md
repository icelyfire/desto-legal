# Desto — pagine legali e di supporto

Pagine pubbliche di Desto, utility per macOS che impedisce lo sleep del Mac dalla
barra dei menu. Ospitate con GitHub Pages, usate come URL richiesti da App Store
Connect. Disponibili in italiano e inglese.

## URL

| Lingua | Supporto (*Support URL*) | Privacy (*Privacy Policy URL*) |
|---|---|---|
| 🇮🇹 Italiano | <https://icelyfire.github.io/desto-legal/> | <https://icelyfire.github.io/desto-legal/privacy.html> |
| 🇬🇧 English | <https://icelyfire.github.io/desto-legal/en/> | <https://icelyfire.github.io/desto-legal/en/privacy.html> |

Su App Store Connect gli URL italiani vanno nella localizzazione italiana della scheda,
quelli inglesi nella localizzazione inglese.

## Struttura

```
index.html         supporto (IT)
privacy.html       privacy (IT)
en/index.html      supporto (EN)
en/privacy.html    privacy (EN)
style.css          stile condiviso da tutte le pagine
```

Ogni pagina ha in intestazione un selettore di lingua e dichiara le alternative con
`hreflang`. Nessuna dipendenza oltre ai font Google.

## Modifiche

Le pagine sono HTML statico: si modificano direttamente e vengono pubblicate al push
su `main`. Due accortezze:

- una modifica ai contenuti va riportata in **entrambe** le lingue;
- quando cambia l'informativa sulla privacy va aggiornata anche la data di entrata in
  vigore, presente sia in `privacy.html` sia in `en/privacy.html`.

## Anteprima locale

```
python3 -m http.server 8899
```

Poi apri <http://localhost:8899>.
