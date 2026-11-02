# AXORA Updates

Готові оновлення AXORA. Завантаження **без токена, пароля чи акаунта GitHub**.

## Калібратор Windows 1.1.3

[Завантажити AXORA Calibrator 1.1.3](https://raw.githubusercontent.com/ArKru75/AXORA-Updates/main/calibrator/AXORA-Calibrator-1.1.3.zip)

Розпакуйте ZIP та запустіть **AxoraCalibrator.exe**. У розділі **Прошивка**
натисніть **Перевірити GitHub**, потім **Оновити прошивку**, якщо доступна новіша версія.
Для запису потрібен AVRDUDE з установленого пакета Arduino AVR Boards.
Перед записом калібратор створює резервну копію та перевіряє HEX/SHA-256.
Після запису перевіряє версію й збережені дані.

## Прошивка 2.1.10

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
This repository distributes binaries and update metadata only.
