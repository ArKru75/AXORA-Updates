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

## Калібратор Windows 1.1.18

[Завантажити AXORA Calibrator 1.1.18](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.18.zip)

У «Підсвічуванні» доступні яскравість і один тест «Веселка». Прошивка 2.1.19 зберігає профіль за вибраною моделлю: AXORA — 3 світлодіоди, AXORA Pro — 7. Тест показує сім кольорів по одному за секунду.

Поруч із моделлю виберіть режим «Звичайний» або «Експерт». У звичайному доступні Калібрування, Налаштування та Підсвічування. У режимі «Експерт» доступні всі розділи, зокрема Центри датчиків і Журнал. Вибір зберігається між запусками.

Розпакуйте ZIP та запустіть **AxoraCalibrator.exe**. У режимі **Експерт** у розділі **Оновлення**
натисніть **Перевірити оновлення**, потім **Оновити прошивку**, якщо доступна новіша версія.
Для запису потрібен AVRDUDE з установленого пакета Arduino AVR Boards.
При звичайному оновленні AXORA створюється резервна копія. HEX/SHA-256
перевіряються перед записом в обох режимах.
Для нової плати або повторного запису відкрийте **Експерт → Оновлення → Сервісне встановлення**,
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

## Прошивка 2.1.19 — підсвічування

Виберіть модель у калібраторі. Пристрій зберігає профіль із **3 світлодіодами
для AXORA** або **7 для AXORA Pro**. Яскравість можна змінити й зберегти
в розділі **Підсвічування**. Кнопка **Тест «Веселка»** показує сім кольорів
і повертає звичайну індикацію. Повторне натискання зупиняє тест.

### Призначення кнопок

У калібраторі 1.1.18 відкрийте **Експерт → Кнопки** і виберіть одну з
15 кнопок SpaceMouse Pro Wireless для кожної фізичної кнопки AXORA.
Наприклад, для кнопки 1 виберіть **Escape**. Натисніть **Зберегти призначення**,
щоб записати призначення в AXORA, і ввімкніть CAD.
Зайняті HID-призначення зникають зі списків інших кнопок. Якщо на пристрої
вже є дублікати, усуньте їх перед збереженням.
У режимі **AXORA Pro** тест перевіряє всі дев’ять фізичних кнопок із призупиненим CAD.

Для встановлення відкрийте **Експерт → Оновлення → Перевірити оновлення → Оновити прошивку**.
Калібратор створює резервну копію калібрування, перевіряє HEX, версію
та збережені дані. Збірка 2.1.19 перевірена для ATmega32U4. Переназначення
перевірено автоматичними тестами калібратора та звірено з профілем 3DxWare.
На фізичній платі цю версію ще не перевіряли.

[HEX 2.1.19](updates/firmware/AXORA-2.1.19-CAD.hex) · [Опис оновлення](updates/stable.json) · [Схема підключення кнопок](docs/AXORA-Nine-Buttons-UA.md)

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
Select Normal or Expert next to the model. Normal shows Calibration, Settings and Lighting. Expert shows all sections, including Sensor centers and Log. Your selection is saved between launches.
Use **Expert → Updates → Check for updates → Update firmware**. The calibrator validates the
download, backs up calibration and verifies the programmed version and retained data.
Use the global **CAD** button to turn model control on or off from any workspace.
Lighting offers brightness controls and one Rainbow test. Firmware 2.1.19 stores the selected model profile: 3 LEDs for AXORA or 7 for AXORA Pro. The test shows seven colors, one per second.

In Expert → Buttons, select one of 15 SpaceMouse Pro Wireless HID assignments for each physical button, such as Escape. Click Save assignments, then enable CAD. Remapping requires Calibrator 1.1.18 and firmware 2.1.18. AXORA Pro tests all nine physical buttons with CAD paused.
This repository distributes binaries and update metadata only.

The Install / reflash board service mode requires the owner-configured master
password for each flash. Normal AXORA updates do not require this password.
Version 1.1.7 remains withdrawn; its detection has not been reclassified.
