# Интеграция с Nexus 2

Чтобы скачать приложение из репозитория Nexus 2, кроме, собственно, названия репозитория потребуются параметры `group_id`, `artifact_id` и `version`. Кроме этого, необходимо выбрать систему дистрибуции (параметр `distribution_system nexus2`), а также указать следующие обязательные параметры:

* `nexus2_url` — URL сервера Nexus 2, на котором находится мобильное приложение.
* `nexus2_login` — имя пользователя на сервере Nexus 2 с правами доступа к репозиторию, где находится мобильное приложение.
* `nexus2_password` — пароль для учетной записи на сервере Nexus 2 с правами доступа к репозиторию, где находится мобильное приложение.
* `nexus2_repo_name` — имя репозитория Nexus 2, где находится мобильное приложение.
* `nexus2_group_id` — `group_id` загруженного мобильного приложения из данных **maven**.
* `nexus2_artifact_id` — `artifact_id` загруженного мобильного приложения из данных **maven**.
* `nexus2_version` — версия загруженного мобильного приложения из данных **maven**.
* `nexus2_extension` — расширение мобильного приложения.

Также, используя опциональный параметр `nexus2_file_name`, можно указать имя файла, с которым необходимо сохранить скачиваемое приложение.

Для загрузки приложения в **Nexus** можно использовать либо [сниппет для Android](https://gist.github.com/Dynamic-Mobile-Security/9730e8eaa1b5d5f7f21e28beb63561a8) (\*. apk), либо — [для iOS](https://gist.github.com/Dynamic-Mobile-Security/66daaf526e0109636d8bcdc21fd10779) (*.ipa).

## Пример запуска

Чтобы скачать приложение с Nexus 2, выполните следующую команду:

    python mdast_cli/mdast_scan.py -d -ds nexus2 \
        --nexus2_url http://nexus:8081/nexus/ \
        --nexus2_login login \
        --nexus2_password password \
        --nexus2_repo_name repo \
        --nexus2_group_id com.swdf.buggen \
        --nexus2_artifact_id app-prod-debug \
        --nexus2_version 1.337 \
        --nexus2_extension apk \
        --nexus2_file_name b3st_file_fr0m_nexus2
