# Интеграция с RuStore

Интеграция с Rustore осуществляется с помощью скрипта [mdast_scan.py](https://github.com/Dynamic-Mobile-Security/mdast-cli).

## Сбор необходимых параметров

Чтобы скачать приложение с [RuStore](https://www.rustore.ru/), необходимо знать имя пакета. При запуске скрипта оно передается с параметром `rustore_package_name`.

<figure markdown>![](./img/49.png)</figure>

Кроме этого, потребуется указать соответствующую систему дистрибьюции (`distribution_system rustore`).

## Примеры запуска скрипта

!!! note "Примечание"
    Более подробная информация о параметрах запуска скрипта приведена в разделе «[Системы CI/CD/Параметры запуска](./sistemy_ci_cd.md#_4)».

После сбора необходимых параметров можно, запустив скрипт, скачать приложение и запустить его сканирование.

### Запуск сканирования с использованием предварительно записанного тест-кейса

``` bash hl_lines="2"
mdast_cli \
  --testcase_id 4 # (1)
  --distribution_system file
  --file_path "/files/demo/apk/demo.apk"
  --url "https://saas.mobile.appsec.world"
  --profile_id 1
  --company_id 1
  --architecture_id 1
  --token "eyJ**********QiLbJhcGciO5JIU4I1NiJ1..."
```

1. Идентификатор предварительно записанного тест-кейса

### Запуск сканирования без тест-кейса

``` bash
mdast_cli
  --distribution_system file
  --file_path "/files/demo/apk/demo.apk"
  --url "https://saas.mobile.appsec.world"
  --profile_id 1
  --company_id 1
  --architecture_id 1
  --token "eyJ**********1QiLbJhcGciO5JIU4I1NiJ1..."
```