# Перезагрузка сервера без обновления Стингрей

Если необходимо перезагрузить сервер, на котором установлен Стингрей, например, для обновления операционной системы, без обновления версии Стингрей, перед перезагрузкой сервера в папке, указанной при генерации конфигурации (в примере `/opt/stingray`), выполните команду:

    docker exec stingray-maintenance django-admin maintenance engines preserve

После перезагрузки сервера там же выполните команду:

    docker exec stingray-maintenance django-admin maintenance engines restore

.