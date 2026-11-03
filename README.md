# AXORA Updates

Готові оновлення AXORA. Завантаження **без токена, пароля чи акаунта GitHub**.

## Посібник користувача

[Ілюстрований PDF-посібник українською](docs/AXORA-User-Guide-UA.pdf).
[Пряме посилання на PDF для NFC](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/docs/AXORA-User-Guide-UA.pdf).
Адреса посібника не містить номера версії та зберігається при оновленнях.

[Встановлення та перепрошивання плати](docs/AXORA-Board-Installation-UA.md) · [Сервісний доступ](docs/AXORA-Service-Mode-UA.md)

## Калібратор Windows 1.1.10

[Завантажити AXORA Calibrator 1.1.10](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.10.zip)

Розпакуйте ZIP та запустіть **AxoraCalibrator.exe**. У розділі **Прошивка**
натисніть **Перевірити GitHub**, потім **Оновити прошивку**, якщо доступна новіша версія.
Для запису потрібен AVRDUDE з установленого пакета Arduino AVR Boards.
При звичайному оновленні AXORA створюється резервна копія. HEX/SHA-256
перевіряються перед записом в обох режимах.
Для нової плати або повторного запису відкрийте **Встановлення / перепрошивання**,
виберіть USB-порт і підтвердьте Pro Micro 5 В / 16 МГц із Caterina.
Цей сервісний режим потребує мастер-пароля на кожен запис.
Кнопка **Прошити плату автоматично** не потребує ручного RESET, якщо поточний
скетч підтримує USB COM і перезапуск на 1200 бод. Інакше потрібен ISP.
Попередній скетч замінюється без копії; після першого запису виконайте навчання.
Після запису перевіряє версію й збережені дані.

Кнопка **CAD** у верхній частині вікна вмикає та вимикає керування моделлю
з будь-якої вкладки. Стан підтверджується пристроєм; повторні кліки під час
перемикання блокуються. Окремих кнопок CAD/HID у «Перевірка рухів» більше немає.

Після підключення індикатори окремо показують навчену матрицю та стан центру.
Якщо видно **Матриця навчена / Центр не підтверджено**, відпустіть рукоятку й
кнопки й зачекайте повторної перевірки приблизно 3–5 секунд у прошивці 2.1.14.
Якщо центр не підтверджується, виконайте **Лише центр**. Матриця зберігається.

## Прошивка 2.1.15

У калібраторі відкрийте **RGB**. **Кількість світлодіодів**: 1-16, типово 3;
натисніть **Зберегти кількість**, щоб застосувати її до індикації та тестів
і залишити після перепідключення. Для цього потрібна прошивка 2.1.15.
Також доступні яскравість 0–100%, попередній
перегляд без EEPROM і кнопка **Зберегти яскравість**. R/G/B/W або циклічний тест
припиняється через 10 секунд чи кнопкою **Зупинити тест**. Матриця зберігається.

AXORA HW1 / ATmega32U4, CAD USB VID **256F**, PID **C631**.
Використовуйте калібратор для перевірки сумісності та запису.
[Дані актуальної прошивки](updates/stable.json) · [Контрольні суми](SHA256SUMS.txt)

У цьому репозиторії лише готові пакети й дані оновлення.
Вихідний код і персональні файли калібрування тут не публікуються.
Пакети версій зберігаються під незмінними іменами.

## Попередній пакет 1.1.7

Пакет 1.1.7 залишається вилученим через виявлення Microsoft Defender
Program:Script/Wacapew.A!ml. Його не перевидавали; причина попереднього
виявлення не оголошується хибним спрацюванням. Версія 1.1.10 є окремою
збіркою з новими функціями; її EXE та ZIP перевірені локальним Defender
03.11.2026 без виявлень.

## English

Ready-to-install AXORA updates. No token, password or GitHub account is needed.
Download the Windows ZIP above, extract it and run AxoraCalibrator.exe.
Use **Firmware → Check GitHub → Update firmware**. The calibrator validates the
download, backs up calibration and verifies the programmed version and retained data.
Use the global **CAD** button to turn model control on or off from any workspace.
This repository distributes binaries and update metadata only.

The Install / reflash board service mode requires the owner-configured master
password for each flash. Normal AXORA updates do not require this password.
Version 1.1.7 remains withdrawn; its detection has not been reclassified.
