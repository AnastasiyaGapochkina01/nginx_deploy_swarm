Структура репозитория
```
├── docker-compose.yml
└── nginx
    ├── app
    │   └── index.html
    ├── default.conf
    └── Dockerfile
```
Решение задачи максимально простое, без "наворотов":
- имеем два стейджа в пайплайне build и deploy
- runner запущен на той же машине, где проиходит билд и деплой (экономия ресурсов)
- registry используем от gitlab
- в build непосредственно собираем image и пушим в registry
- в deploy деплоим
