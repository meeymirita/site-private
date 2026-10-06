# site-private

Служебные страницы сайта [anitech.meeymirita.ru](https://anitech.meeymirita.ru), подключены подмодулем `site-private` в [anitech-performance](https://github.com/meeymirita/anitech-performance).

| Путь | Что | URL на сайте |
|---|---|---|
| `mira/index.html` | личная шпаргалка владельца (закрыта паролем в Caddy, `deploy/protect-mira.sh`) | `/mira/` |
| `mira-login/index.html` | форма входа в шпаргалку | `/mira-login/` |
| `404.html` | страница «не найдено» (Caddy отдаёт её через `rewrite * /404.html`) | любой несуществующий адрес |

Скрипт `deploy/deploy-site.sh` родителя выкладывает эти файлы в корень сайта: `site-private/mira/` → `/mira/`, `site-private/mira-login/` → `/mira-login/`, `site-private/404.html` → `/404.html`. Пароли и ключи сюда не пишем — только их названия.

Статус: служебный репозиторий, не лаба.
