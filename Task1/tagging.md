# Тегирование

## Теги

`class`: public | internal | pii | special | secret  
`purpose`: registration | care | payment | warehouse | analytics  
`retention`: e.g. medical:5y, logs:90d  
`protection`: encrypt | mask | anonymize  
`owner`: Reception | Care | Finance | Warehouse | IT

Пример: `medical_record.diagnosis` → `class=special; purpose=care; retention=5y; protection=encrypt; owner=Care`

## Инструменты

| Слой | Инструмент |
|------|------------|
| Каталог | DataHub / OpenMetadata |
| Файлы | метки файлового сервера / S3 tags (to-be) |
| БД | комментарии колонок + policy-as-code |
| Lineage | OpenLineage → DataHub |
| Runtime DLP | Microsoft Purview / аналог |
| CI | проверка: special без protection = fail |
