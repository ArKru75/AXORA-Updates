# AXORA Updates

Готові оновлення AXORA. Завантаження **без токена, пароля чи акаунта GitHub**.

## Калібратор Windows 1.1.6

[Завантажити AXORA Calibrator 1.1.6](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.6.zip)

Розпакуйте ZIP та запустіть **AxoraCalibrator.exe**. У розділі **Прошивка**
натисніть **Перевірити GitHub**, потім **Оновити прошивку**, якщо доступна новіша версія.
Для запису потрібен AVRDUDE з установленого пакета Arduino AVR Boards.
Перед записом калібратор створює резервну копію та перевіряє HEX/SHA-256.
Після запису перевіряє версію й збережені дані.

Кнопка **CAD** у верхній частині вікна вмикає та вимикає керування моделлю
з будь-якої вкладки. Стан підтверджується пристроєм; повторні кліки під час
перемикання блокуються. Окремих кнопок CAD/HID у «Перевірка рухів» більше немає.

Після підключення індикатори окремо показують навчену матрицю та стан центру.
Якщо видно **Матриця навчена / Центр не підтверджено**, відпустіть рукоятку й
кнопки й зачекайте повторної перевірки приблизно 3–5 секунд у прошивці 2.1.14.
Якщо центр не підтверджується, виконайте **Лише центр**. Матриця зберігається.

## Прошивка 2.1.14

У калібраторі відкрийте **RGB** — яскравість 0–100%, попередній
перегляд без EEPROM і кнопка **Зберегти яскравість**. R/G/B/W або циклічний тест
припиняється через 10 секунд чи кнопкою **Зупинити тест**. Матриця зберігається.

AXORA HW1 / ATmega32U4, CAD USB VID **256F**, PID **C631**.
Використовуйте калібратор для перевірки сумісності та запису.
[Дані актуальної прошивки](updates/stable.json) · [Контрольні суми](SHA256SUMS.txt)

У цьому репозиторії лише готові пакети й дані оновлення.
Вихідний код і персональні файли калібрування тут не публікуються.
Пакети версій зберігаються під незмінними іменами.

## English

Ready-to-install AXORA updates. No token, password or GitHub account is needed.
Download the Windows ZIP above, extract it and run AxoraCalibrator.exe.
Use **Firmware → Check GitHub → Update firmware**. The calibrator validates the
download, backs up calibration and verifies the programmed version and retained data.
Use the global **CAD** button to turn model control on or off from any workspace.
This repository distributes binaries and update metadata only.
