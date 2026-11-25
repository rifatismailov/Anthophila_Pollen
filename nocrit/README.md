# Лише виявлення ШПЗ (`nocrit`)

Правила виявлення ШПЗ (джерела і власні), без критичних правил і без списків.

**Склад:** правила виявлення джерел, власні правила.

| | |
|---|---|
| Версія правил | **v1.0.6** (2026-11-25) |
| Файлів у пакеті | 1668 |
| sha256 пакета | `08ab19fe64273403cdc5d75e7054c14ca39ffd13bde0454a00323403da6d117a` |
| Ключ підпису правил | `ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=` |

## Файли

| Файл | Що це |
|---|---|
| `rules-manifest.json` | маніфест: версія, sha256 пакета і кожного файлу |
| `rules-manifest.sig` | підпис маніфесту (ed25519) |
| `DocScan-rules.zip` | пакет правил |
| `DocScan-rules-bundle.zip` | ці три файли в одному — для ручного встановлення |

## Підключити ПК

```json
{
  "mode": "mirror",
  "mirror": { "url": "<дзеркало програми DocScan, як і зараз>" },
  "rules": { "mirror": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/nocrit" } },
  "extra_public_keys": [ "ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=" ]
}
```

Вручну на одному ПК: `docscan-updater.exe -InstallRules DocScan-rules-bundle.zip`.

[← усі редакції](../README.md)
