# dosbox-ded32 (repacked)

Этот репозиторий содержит перепакованную версию архива с досом Деда:
[https://ded32.net.ru/](https://ded32.net.ru/)

## Что это такое

Оригинальный архив распространяется в формате `RAR SFX` (`.rar.exe`) который проблематично распаковать с Linux/MacOS.

## Решение

Архив был:

1. Распакован в совместимой среде
2. Перепакован в стандартный формат `tar.gz`
3. Разбит на несколько частей (`part_aa`, `part_ab`), чтобы обойти ограничения GitHub по размеру файлов

## Как скачать и распаковать

Выполните одну команду:

```bash
curl -L \
  curl -L \
  https://raw.githubusercontent.com/Neburalis/dosbox-ded32/main/dosbox-asm-setup.tar.gz.part_aa \
  https://raw.githubusercontent.com/Neburalis/dosbox-ded32/main/dosbox-asm-setup.tar.gz.part_ab \
| cat > dosbox-asm-setup.tar.gz && tar -xzf dosbox-asm-setup.tar.gz
```

## Что делает команда

* скачивает обе части архива напрямую с GitHub (raw)
* объединяет их в один файл `dosbox-asm-setup.tar.gz`
* распаковывает содержимое
