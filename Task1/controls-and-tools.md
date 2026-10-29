# Меры и инструменты по потокам

| Мера | Потоки | Зачем |
|------|--------|-------|
| TLS + VPN/частная сеть | все | in-transit |
| BitLocker / TDE / KMS | диск, 1С, медхранилище | at-rest |
| AD RBAC + ABAC на медданные | 1, 2, 5 | least privilege |
| Шифрование файлов медкарт | 2, 5 | special |
| DLP на Exchange | 1 | утечки почты |
| Audit log + алерты | все чтения special | accountability |
| Anonymizer перед BI | 6 | minimization |
| DataHub + OpenLineage | все | теги + lineage |
| Consent / право на удаление | портал (to-be) | 152-ФЗ |
| Запрет копий на ПК аналитика | 6 | PbD default |

| Практика | As-Is | To-Be |
|----------|-------|-------|
| Privacy by Design | нет | теги, CI, раздельные домены |
| Data Minimization | полные файлы всем | DTO по роли + анон для BI |
| Data Lineage | нет | OpenLineage |
