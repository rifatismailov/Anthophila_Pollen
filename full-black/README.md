# Повна без білого списку (`full-black`)

Усі правила і чорний список, без білого: кожен файл сканується, винятків немає.

**Склад:** правила виявлення джерел, власні правила, критичні правила, чорний список.

| | |
|---|---|
| Версія правил | **v1.0.6** (2026-11-25) |
| Файлів у пакеті | 1669 (критичних: 1) |
| sha256 пакета | `4fa1739053474485f18749513ab5f3079fea8cd4226e2be57d2da379d06186b0` |
| Ключ підпису правил | `ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=` |
| Чорний список | serial 20261125140619, записів: 110 |
| Ключ підпису списків | `ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=` |

## Файли

| Файл | Що це |
|---|---|
| `rules-manifest.json` | маніфест: версія, sha256 пакета і кожного файлу |
| `rules-manifest.sig` | підпис маніфесту (ed25519) |
| `DocScan-rules.zip` | пакет правил |
| `DocScan-rules-bundle.zip` | ці три файли в одному — для ручного встановлення |
| `blacklist.json` / `.sig` | чорний список і його підпис |

## Підключити ПК

```json
{
  "mode": "mirror",
  "mirror": { "url": "<дзеркало програми DocScan, як і зараз>" },
  "rules": { "mirror": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/full-black" } },
  "extra_public_keys": [ "ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=" ],
  "lists": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/full-black", "public_keys": [ "ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=" ] }
}
```

Вручну на одному ПК: `docscan-updater.exe -InstallRules DocScan-rules-bundle.zip`.

[← усі редакції](../README.md)
