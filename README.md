# Anthophila_Pollen

Правила й списки для **DocScan**, які публікує [Anthophila_Hive](https://github.com/rifatismailov/Anthophila_Hive)
(простір `org-example`). Поточна версія правил: **v1.0.6** (2026-11-25).

Кожна тека — окрема **редакція**: свій склад і свій підписаний пакет. ПК читають лише теку своєї редакції.

| Редакція | Склад | Тека |
|---|---|---|
| [Повна](full/) | правила виявлення джерел, власні правила, критичні правила, білий список, чорний список | `full/` |
| [Повна без білого списку](full-black/) | правила виявлення джерел, власні правила, критичні правила, чорний список | `full-black/` |
| [Без критичних правил, з чорним списком](nocrit-black/) | правила виявлення джерел, власні правила, чорний список | `nocrit-black/` |
| [Лише виявлення ШПЗ](nocrit/) | правила виявлення джерел, власні правила | `nocrit/` |
| [Лише правила джерел](vendor/) | правила виявлення джерел | `vendor/` |
| [Лише списки](lists/) | білий список, чорний список | `lists/` |

## Як підключити ПК (DocScanUpdater, `updater.json`)

Адреса редакції для ПК: `https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/<редакція>`.
Приклад — редакція `full`:

```json
{
  "mode": "mirror",
  "mirror": { "url": "<дзеркало програми DocScan, як і зараз>" },
  "rules": { "mirror": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/full" } },
  "extra_public_keys": [ "ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=" ],
  "lists": { "url": "https://raw.githubusercontent.com/rifatismailov/Anthophila_Pollen/main/full", "public_keys": [ "ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=" ] }
}
```

* Правила з дзеркала DocScanUpdater бере лише в режимі `"mode": "mirror"`; у цьому режимі потрібна й адреса
  дзеркала самої програми (`mirror.url`). Списки (`lists.url`) працюють у будь-якому режимі.
* ПК довіряють лише підписаному: пакет правил — ключем `ed25519:2vfxMxxGiMm8CVAnXqC173tSP3FKFOS2tMIn8YBTM5k=` (його додають у `extra_public_keys`),
  списки — ключем `ed25519:38vUbyKunP0WdBwik2KP2RYJxI+mur24avZLWK2VX+o=` (`lists.public_keys`). Підпис і sha256 кожного файлу перевіряються до встановлення;
  старішої версії за встановлену ПК не ставлять.
* Встановити вручну: `docscan-updater.exe -InstallRules DocScan-rules-bundle.zip` (файл з теки редакції).

Тут завжди лише остання версія кожної редакції; історія релізів — в Anthophila_Hive.
Не змінюйте файли вручну — ПК їх відкинуть; наступна публікація все одно перезапише теку.

<sub>Згенеровано Anthophila_Hive 0.3.0.</sub>
