# short-whitelist

Автоматически обновляемый сокращенный whitelist.

Репозиторий собирает итоговый список из нескольких публичных источников и публикует готовый файл в `data/short-whitelist.txt`.

## Что делает сборка

- Берет первые `40` строк из основного источника без изменений.
- Добавляет случайную выборку из `160` строк из оставшейся части основного источника и дополнительных списков.
- Пересобирает файл каждые `6` часов через GitHub Actions.

## Источники

- `https://raw.githubusercontent.com/zieng2/wl/main/vless_lite.txt`
- `https://raw.githubusercontent.com/igareck/vpn-configs-for-russia/refs/heads/main/Vless-Reality-White-Lists-Rus-Mobile.txt`
- `https://raw.githubusercontent.com/igareck/vpn-configs-for-russia/refs/heads/main/Vless-Reality-White-Lists-Rus-Mobile-2.txt`

## Готовый файл

- `data/short-whitelist.txt`

## Локальный запуск

```bash
python scripts/update.py
```
