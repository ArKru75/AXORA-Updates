# AXORA Updates

Готові оновлення AXORA. Завантаження **без токена, пароля чи акаунта GitHub**.

## Посібники користувача / User guides

Два прості ілюстровані посібники для **калібратора 1.1.10**: по 13 сторінок,
усі 12 рухів калібрування, налаштування, підсвічування та швидка допомога.
Редакція від **06.11.2026**.

- [Українською - PDF](docs/AXORA-User-Guide-UA.pdf) · [Завантажити](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/docs/AXORA-User-Guide-UA.pdf)
- [English - PDF](docs/AXORA-User-Guide-EN.pdf) · [Download](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/docs/AXORA-User-Guide-EN.pdf)

Обидві адреси не містять номера версії. Чинне українське посилання для NFC збережено.
[Усі посилання та NFC](docs/README.md).

[Встановлення та перепрошивання плати](docs/AXORA-Board-Installation-UA.md) · [Сервісний доступ](docs/AXORA-Service-Mode-UA.md)

## Драйвер для CAD / CAD driver

Для роботи AXORA з CAD-програмами встановіть **3Dconnexion 3DxWare** для Windows або macOS.
[Офіційне завантаження / Official download](https://3dconnexion.com/us/drivers/).
To use AXORA in CAD, install **3Dconnexion 3DxWare** for Windows or macOS.
Калібратор працює у Windows. / The calibrator runs on Windows.

## Калібратор Windows 1.1.12

[Завантажити AXORA Calibrator 1.1.12](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.12.zip)

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

## Прошивка 2.1.17 — дев’ять кнопок CAD

Додано шість кнопок: **FIT, Rotation Lock, Roll+, TopView, RightView, FrontView**.
Початкові кнопки 1, 2, 3 та їхні сервісні комбінації збережено.
[Піни, підключення до GND та перевірка](docs/AXORA-Nine-Buttons-UA.md).

Збережено виправлення затримок USB Serial з 2.1.16. Матриця калібрування,
параметри рухів та RGB сумісні. Додаткові кнопки працюють у CAD;
у Slicer початкові три кнопки зберігають попередню поведінку.

Оновлення: **калібратор 1.1.12 → Прошивка → Перевірити GitHub → Оновити прошивку**.
Відпустіть рукоятку й усі кнопки під час перезапуску. Калібратор створює
резервну копію, перевіряє HEX, версію та збережені дані.
У калібраторі 1.1.12 виберіть **AXORA Pro → Перевірка кнопок**. Після перевірки
кнопок 1–3 калібратор тимчасово вмикає CAD для перевірки кнопок 4–9.
Тримайте рукоятку в нейтралі й натисніть **Завершити перевірку**, щоб призупинити CAD.
Збірка пройшла CI; фізичне підключення нових кнопок потребує перевірки після встановлення.

[HEX 2.1.17](updates/firmware/AXORA-2.1.17-CAD.hex) · [Опис оновлення](updates/stable.json)

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

[English user guide (PDF)](docs/AXORA-User-Guide-EN.pdf) · [Ukrainian user guide (PDF)](docs/AXORA-User-Guide-UA.pdf).
Both guides cover Calibrator 1.1.10 in 13 illustrated pages.

Download the Windows ZIP above, extract it and run AxoraCalibrator.exe.
Use **Firmware → Check GitHub → Update firmware**. The calibrator validates the
download, backs up calibration and verifies the programmed version and retained data.
Use the global **CAD** button to turn model control on or off from any workspace.
Firmware **2.1.17** adds FIT, Rotation Lock, Roll+, TopView, RightView and FrontView on six free Pro Micro GPIOs. Original buttons1/2/3 and service chords are retained. Select **AXORA Pro → Button test** in Calibrator 1.1.12 to test all nine buttons. Each normally open button connects its GPIO to GND. See the wiring table above.
This repository distributes binaries and update metadata only.

The Install / reflash board service mode requires the owner-configured master
password for each flash. Normal AXORA updates do not require this password.
Version 1.1.7 remains withdrawn; its detection has not been reclassified.
