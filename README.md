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

## Калібратор Windows 1.1.15

[Завантажити AXORA Calibrator 1.1.15](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.15.zip)

Компактний інтерфейс українською та англійською. Підключення і CAD у спільній верхній панелі. У таблиці AXORA Pro видно всі дев’ять кнопок. Журнал і центри датчиків доступні в «Додатково», встановлення плати — в розділі «Оновлення».

Розпакуйте ZIP та запустіть **AxoraCalibrator.exe**. У розділі **Оновлення**
натисніть **Перевірити оновлення**, потім **Оновити прошивку**, якщо доступна новіша версія.
Для запису потрібен AVRDUDE з установленого пакета Arduino AVR Boards.
При звичайному оновленні AXORA створюється резервна копія. HEX/SHA-256
перевіряються перед записом в обох режимах.
Для нової плати або повторного запису відкрийте **Оновлення → Сервісне встановлення**,
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
Якщо видно **Калібрування збережено / Центр не підтверджено**, відпустіть рукоятку й
кнопки й зачекайте повторної перевірки приблизно 3–5 секунд у прошивці 2.1.14.
Якщо центр не підтверджується, виконайте **Лише центр**. Матриця зберігається.

## Прошивка 2.1.18 — призначення кнопок HID

У калібраторі 1.1.15 відкрийте **Кнопки** і виберіть одну з
15 кнопок SpaceMouse Pro Wireless для кожної фізичної кнопки AXORA.
Наприклад, для кнопки 1 виберіть **Escape**. Натисніть **Зберегти призначення**,
щоб записати призначення в AXORA, і ввімкніть CAD.
Зайняті HID-призначення зникають зі списків інших кнопок. Якщо на пристрої
вже є дублікати, усуньте їх перед збереженням.
У режимі **AXORA Pro** тест перевіряє всі дев’ять фізичних кнопок із призупиненим CAD.

Для встановлення відкрийте **Оновлення → Перевірити оновлення → Оновити прошивку**.
Калібратор створює резервну копію калібрування, перевіряє HEX, версію
та збережені дані. Збірка 2.1.18 перевірена для ATmega32U4. Переназначення
перевірено автоматичними тестами калібратора та звірено з профілем 3DxWare.
На фізичній платі цю версію ще не перевіряли.

[HEX 2.1.18](updates/firmware/AXORA-2.1.18-CAD.hex) · [Опис оновлення](updates/stable.json) · [Схема підключення кнопок](docs/AXORA-Nine-Buttons-UA.md)

У калібраторі відкрийте **Підсвічування**. **Кількість світлодіодів**: 1-16, типово 3;
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
Use **Updates → Check for updates → Update firmware**. The calibrator validates the
download, backs up calibration and verifies the programmed version and retained data.
Use the global **CAD** button to turn model control on or off from any workspace.
In Button test, select one of 15 SpaceMouse Pro Wireless HID assignments for each physical button, such as Escape. Click Save assignments, then enable CAD. Remapping requires Calibrator 1.1.15 and firmware 2.1.18. AXORA Pro tests all nine physical buttons with CAD paused.
This repository distributes binaries and update metadata only.

The Install / reflash board service mode requires the owner-configured master
password for each flash. Normal AXORA updates do not require this password.
Version 1.1.7 remains withdrawn; its detection has not been reclassified.
