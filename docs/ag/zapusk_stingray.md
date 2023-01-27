# Запуск Stingray

!!! note "Примечание"
    В этом разделе описан процесс первого запуска версии системы Stingray. Процесс запуска Stingray после обновления версии описан в разделе «[Обновление системы](./obnovlenie_sistemy.md)». Процесс запуска Stingray после перезагрузки сервера без обновления версии Stingray описан в разделе «[Перезагрузка сервера без обновления Stingray](./perezagruzka_servera_bez_obnovleniya_stingray.md)».

Для запуска приложения в папке, указанной при генерации конфигурации (в примере ***/opt/stingray***) выполните команды:

    docker-compose pull
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/android_api27:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/android_api30:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/ios:latest
    docker-compose up -d

!!! note "Примечание"
    Версия релиза может быть указана двумя способами. Если она указана как `latest`, будет использована версия последнего релиза Stingray. Пожалуйста, уточняйте эту информацию у вендора или на официальном сайте. Также может быть указана версия конкретного релиза, например, например, 2022.08 или 2022.10. В этом случае будет команда может выглядеть, например, следующим образом:

        docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/android_api27:2022.10


При первом запуске системы, если команда docker-compose не может загрузить образ из репозитория, необходимо вручную загрузить контейнеры:

    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/stingray:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/android_api27:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/android_api30:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/ios:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/stingray-ui:latest
    docker pull cr.yandex/crp8p3a3l1ri2431n3ce/release/stingray-knowledgebase:latest

!!! note "Примечание"
    Версия релиза может быть указана двумя способами. Если она указана как `latest`, будет использована версия последнего релиза Stingray. Пожалуйста, уточняйте эту информацию у вендора или на официальном сайте. Также может быть указана версия конкретного релиза, например, например, 2022.08 или 2022.10.