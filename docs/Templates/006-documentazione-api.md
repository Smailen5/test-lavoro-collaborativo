# Documentazione API

## Scopo
Descrivere gli endpoint, i parametri, i formati di request/response e gli esempi di utilizzo delle API.

## Sommario
- Autore:
- Data:
- Versione:

## Panoramica
Breve descrizione dell'API, destinatari e casi d'uso principali.

## Autenticazione
- Metodo di autenticazione (es. OAuth2, API Key, JWT)
- Esempio di header:

```
Authorization: Bearer <token>
```

## Voci di endpoint (tabella)
| Endpoint | Metodo | Descrizione | Parametri principali | Response | Codici HTTP |
|----------|--------|-------------|----------------------|----------|-------------|
| /api/items | GET | Elenca gli elementi | page, per_page | JSON array | 200, 401, 500 |

## Esempi di request/response
### GET /api/items
Request:
```
GET /api/items?page=1&per_page=10 HTTP/1.1
Authorization: Bearer <token>
```
Response:
```json
{
  "data": [ ... ],
  "meta": { "page": 1 }
}
```

## Gestione errori
- Struttura degli errori (es. {"error": {"code": "ERR_...", "message": "..."}})
- Codici e significato (400, 401, 403, 404, 500)

## Versioning dell'API
- Politica di versioning (URL versioning, header)

## Limiti e rate limiting
- Limiti per minuto/ora, header di controllo rate

## Note di sicurezza
- Validazione input, evitare leak di dati sensibili

## Cronologia Versioni
- v1.0 - Data - Autore - Note