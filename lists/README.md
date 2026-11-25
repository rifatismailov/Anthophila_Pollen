# Лише списки (`lists`)

Тільки білий і чорний списки — для ПК, що беруть правила з іншого місця.

**Склад:** білий список, чорний список.

| | |
|---|---|
| Білий список | serial 20261125140619, записів: 2 |
| Чорний список | serial 20261125140619, записів: 110 |
| Ключ підпису списків | `ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=` |

## Файли

| Файл | Що це |
|---|---|
| `whitelist.json` / `.sig` | білий список і його підпис |
| `blacklist.json` / `.sig` | чорний список і його підпис |

## Підключити ПК

```json
{
  "lists": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/lists", "public_keys": [ "ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=" ] }
}
```

У цій редакції немає правил: ПК беруть їх з іншого джерела, а списки — звідси (`lists.url` працює в будь-якому режимі).

[← усі редакції](../README.md)
