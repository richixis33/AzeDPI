# ⚡ AzeDPI

<p align="center">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Platform-Android%20%7C%20Linux-blue?style=for-the-badge" alt="Platforms">
  <img src="https://img.shields.io/badge/Fork-ByeByeDPI-orange?style=for-the-badge" alt="Fork">
  <img src="https://img.shields.io/badge/License-GPL--3.0-purple?style=for-the-badge" alt="License">
</p>

<p align="center">
  <b>AzeDPI</b> — модифицированный форк <b>ByeByeDPI</b>, заточенный под агрессивный обход DPI, манипуляцию пакетами и стабильный доступ к Discord, YouTube и заблокированным соцсетям прямо на мобильных устройствах и Linux без использования внешних VPN-серверов.
</p>

---

## 🚀 Почему именно AzeDPI?

В отличие от классического ByeByeDPI, здесь упор сделан на борьбу с современными методами фильтрации (ТСПУ) и оптимизацию под стриминг и войс:

* **Продвинутая фрагментация:** Гибкий сплит ClientHello (SNI/TLS) по кастомным смещениям, сбивающий эвристику большинства DPI-систем.
* **Fake Packets & Desync:** Инъекция мусорных пакетов с низким TTL для десинхронизации анализатора сессий.
* **Discord & Voice Fix:** Оптимизация обработки UDP-трафика и STUN-запросов для нормальной работы голосовых каналов и звонков.
* **YouTube 4K без буферизации:** Точечная модификация заголовков и сплитинг пулов Googlevideo.
* **Нативная скорость:** Трафик не шифруется и не перенаправляется на сторонние прокси — пинг не страдает, оверхед минимален.

---

## 🛠 Ключевые возможности

- [x] **SNI Tripping / Fragmentation:** Разбивка доменного имени в TCP-сегментах на лету.
- [x] **Fake SNI / Header Mangling:** Подмена и деформация параметров запроса.
- [x] **Low-TTL Dummy Packets:** Защита от систем глубокого анализа с помощью пакетов-ловушек.
- [x] **Работа через VpnService (Android):** Полная изоляция и перехват без необходимости рут-прав.
- [x] **CLI-режим для Termux / Linux:** Поддержка работы через `iptables` / `NFQUEUE`.

---

## 📦 Сборка и установка

### Android (APK)

1. Перейди во вкладку [Releases](../../releases) и скачай свежий `AzeDPI.apk`.
2. Установи на устройство, выбери пресет настроек или введи кастомные флаги.
3. Нажми **Connect** и подтверди создание локального VPN-подключения
