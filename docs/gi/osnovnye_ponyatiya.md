# Основные понятия
  
  <p><strong>Проект (Project)</strong> — верхнеуровневая сущность, внутри которой определяются настройки и профили сканирования для конкретного приложения. Каждый проект однозначно связывается со сканируемым приложением (пакетом) либо на этапе создания, либо при первом сканировании. На уровне проекта могут быть переопределены правила сканирования, которые будут применяться только для этого проекта. Имя проекта уникально в рамках системы.</p>
  <p><strong>Профиль (Profile)</strong> — профиль сканирования, включающий в себя настройки каждого модуля, список проверяемых стандартов и требований информационной безопасности. Имя профиля уникально в рамках проекта, к которому он относится.</p>
  <p><strong>Модуль (Module)</strong> — компоненты для сбора различной информации во время сканирования приложения на устройстве (мониторинг системного журнала, использование файлов, операции с базой данных и т. д.). Каждый модуль имеет свои уникальные настройки и может быть зависимым от результатов других модулей.</p>
  <p><strong>Тест кейсы (Test cases)</strong> — записанный сценарий работы пользователя с приложением. Включает в себя все действия пользователя (нажатия, передаваемый текст, любые взаимодействия с интерфейсом приложения и т. д.). Тест кейс привязывается к конкретному проекту и может быть воспроизведен только в рамках него. Тест кейс запускается только если имя приложения (package_id) при запуске совпадает с именем приложения, для которого был записан тест кейс.<br />
    <strong>Сканирование</strong> — процесс анализа, во время которого пользователь вручную или система по записанным ранее тест кейсам взаимодействуют с приложением. Во время сканирования система Stingray собирает всю доступную информацию о работе приложения и затем проводит поиск уязвимостей и проверку на соответствие стандартам безопасности.
  </p>
  <p><strong>Метод сканирования/запуска</strong> — cпособ сканирования, определяющий, запускать ли записанный ранее тест кейс или ожидать ручных операций с приложением. Возможные варианты:</p>
  <ul class="Disc">
    <li><strong>Автоматический</strong> — запускает сканирование и запускает выбранный тест кейс.</li>
    <li><strong>Ручной</strong> — после запуска сканирования необходимо вручную совершать операции с запущенным приложением.</li>
  </ul>
  <p><strong>Имя пакета (Package name)</strong> — имя пакета сканируемого приложения. </p>
  <p><strong>Правила анализа (Rules)</strong> — правила анализа, по которым происходит поиск части уязвимостей. Правила представляют собой набор строк или регулярных выражений, которые необходимо искать в собранных данных. Для удобства добавление правил оформлено в виде конструктора, в котором необходимо указать какую строку искать, в результатах каких модулей и в каком месте данных (XML-тэг, значение в JSON и т. д.).</p>
  <p><strong>Требование (Requirement)</strong> — требования информационной безопасности, на соответствие которому будет проверено приложение. С требованием соотносятся определенные типы дефектов, при нахождении которых в приложении требование будет считаться не выполненным. Требования могут быть сгруппированы в виде категорий или относиться напрямую к стандартам.</p>
  <p><strong>Категория (Category)</strong> — группировка требований информационной безопасности по различным признакам.</p>
  <p><strong>Стандарт (Standard)</strong> — совокупность требований или категорий требований информационной безопасности, на соответствие которым может проверяться приложение. Стандарты могут быть как общемировые, так и внутренние стандарты компании.</p>
  <p><strong>Дефекты (Defects)</strong> — выявленные во время сканирования дефекты приложения или, по-другому, уязвимости. У каждого дефекта есть тип, описание и рекомендации по устранению.</p>
  <p><strong>Собранные данные (Collected Data)</strong> — вся собранная информация о работе приложения за время сканирования. Данные разделены по модулям, каждый из которых отвечает за сбор определенной информации. Эти данные так же можно скачать и проанализировать локально, при желании.</p>
  <p><strong>CI/CD (Continuous Integration / Continuous Delivery)</strong> — системы для непрерывной интеграции и непрерывных поставок приложения. Примерами таких систем могут быть Jenkins, Teamcity, GitLab CI.</p>
  <p><strong>Эмулятор (Emulator)</strong> — виртуальный эмулятор имитирующее реальное устройство Android. Характеризуется различной архитектурой и версией операционной системы.</p>
  <p> </p>