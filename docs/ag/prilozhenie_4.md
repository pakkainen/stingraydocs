# Приложение 4. Appium-скрипты

## Ограничения на используемые Appium-скрипты

Все используемые в системе Appium-скрипты проходят проверку в песочнице, в которой разрешены только следующие Appium-методы/классы, а также команда `sleep`:

	self.sandbox = {
	'driver': driver,
	'sleep': sleep,
	'ActionBuilder': ActionBuilder,
	'ActionChains': ActionChains,
	'AppiumBy': AppiumBy,
	'MultiAction': MultiAction,
	'PointerInput': PointerInput,
	'TouchAction': TouchAction,
	}

## Пример Appium-скрипта

Ниже приведен пример Appium-скрипта, примененного при автоматическом тестировании приложения с пакетом `com.swdf.buggen`.

	el1 = driver.find_element(by=AppiumBy.ID, value="com.swdf.buggen:id/edtMain")
	el1.click()
	el1.send_keys("password=qwerty123")
	el2 = driver.find_element(by=AppiumBy.ID, value="com.swdf.buggen:id/btnGenerate")
	el2.click()
