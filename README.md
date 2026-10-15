# nyutag.chat

Статическая страница приглашений Нютага (GitHub Pages).

- `/i/#XXXX-XXXX` — приглашение: код, кнопка «Открыть в Нютаге» (`nyutag://invite/КОД`), инструкция. Код в `#` не уходит на сервер.
- `/.well-known/assetlinks.json` — Android App Links для `chat.nyutag.messenger` (+ `.debug`).

Сам сервер Нютага здесь не упоминается и через этот сайт не доступен.

## Хостинг (с 15.10.2026)
Сайт раздаёт nginx на НСК (186.246.27.215, `/var/www/nyutag`, конфиг `/etc/nginx/conf.d/nyutag-site.conf`, серт Let's Encrypt через acme.sh). GitHub Pages остался как запасной: DNS в Porkbun — A-записи `@` и `www` → 186.246.27.215 (откат: ALIAS `@` → tsyrenov1987.github.io). Выкладка: `rsync -a --exclude .git --exclude CNAME --exclude README.md ./ nsk:/var/www/nyutag/`.
