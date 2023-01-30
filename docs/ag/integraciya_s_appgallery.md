# Интеграция с AppGallery

Интеграция с AppGallery осуществляется с использованием специального средства инструментальной поддержки — [mdast_cli](https://appgallery.huawei.ru).

При запуске скрипта укажите систему дистрибуции `distribution_system appgallery` и обязательный параметр `appgallery_app_id` — идентификатор пакета скачиваемого приложения.

Чтобы получить `appgallery_app_id`, откройте страницу приложения в браузере и скопируйте параметр из адресной строки браузера.

<figure markdown>![](./img/92.png)</figure>

В данном примере `appgallery_app_id` — `С101184875`.

Также, используя опциональный параметр `appgallery_file_name`, можно указать имя файла, с которым сохранится скачиваемое приложение.

<!-- ## Запуск сканирования с использованием тест-кейса

Укажите параметр `--testcase_id`.

    mdast_cli \
        --testcase_id 4 \
        --distribution_system file \
        --file_path "/files/demo/apk/demo.apk" \
        --url "https://saas.mobile.appsec.world" \
        --profile_id 1 \
        --company_id 1 --architecture_id 1 \
        --token "********************"

## Запуск сканирования без тест-кейса

Не указывайте параметр `--testcase_id`.

    mdast_cli \
        --distribution_system appgallery \
        --appgallery_file_name--file_path "/files/demo/apk/demo.apk" \
        --url "https://saas.mobile.appsec.world" \
        --profile_id 1 \
        --company_id 1 \
        --architecture_id 1 \
        --token "********************" -->
