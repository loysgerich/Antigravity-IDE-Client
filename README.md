# Antigravity IDE Client 🚀
[![Release](https://img.shields.io/github/v/release/loysgerich/Antigravity-IDE-Client?color=blue&label=Stable%20Release)](https://github.com/loysgerich/Antigravity-IDE-Client/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-brightgreen)](#system-requirements)
[![Proxy](https://img.shields.io/badge/Proxy-Port%208047-orange)](#architecture)
[![License](https://img.shields.io/badge/License-Proprietary-red)](#license)

**Antigravity IDE Client** — это официальный GUI-клиент, локальный прокси-сервер и менеджер авторизации для интеграции современных сред разработки (VS Code, JetBrains IDE) с платформой **Antigravity IDE** и **Antigravity 2.0**.

Клиент обеспечивает перенаправление, оптимизацию и безопасность запросов авторизации и взаимодействия с API ассистента программирования на базе искусственного интеллекта.

---

## 🎯 Основные Возможности (Key Features)

* **🔄 Локальный Прокси-Сервер (Порт 8047)**: Мгновенное перенаправление трафика и запросов авторизации/API из плагинов сред разработки на менеджер пула аккаунтов.
* **🍏 Полная Поддержка macOS (Apple Silicon & Intel)**: Автоматический обход ограничений прав TCC (Operation not permitted) и автоматическая ad-hoc переподпись измененных бинарников языкового сервера для предотвращения сбоев ядра (`EXC_BAD_SIGNATURE`).
* **💻 Кроссплатформенность**: Нативные сборки с графическим интерфейсом на базе Tauri для Windows, macOS (aarch64/x64) и Linux (AppImage, deb, rpm).
* **⚡ Экстремальная Производительность**: Мгновенный патчинг языковых серверов (~50 МБ) с использованием оптимизированного алгоритма поиска байт-паттерна (занимает менее 1 секунды).
* **🔒 Безопасность и Конфиденциальность**: Локальная обработка токенов и ключей авторизации без отправки конфиденциальных данных третьим лицам.

---

## 🏗 Архитектура Запросов (Architecture)

Схема маршрутизации запросов авторизации и генерации кода:

```
[ IDE (VS Code / JetBrains / Antigravity IDE) ]
                      │
                      ▼
    [ Локальный прокси Клиента (Port 8047) ]
                      │
                      ▼
    [ Antigravity-Manager (Port 8045 / 8055) ]
                      │
                      ▼
             [ Google Backend ]
```

---

## 🚀 Как Начать Использовать (Quick Start)

1. **Скачайте клиент**: Перейдите в раздел [Релизы (Releases)](https://github.com/loysgerich/Antigravity-IDE-Client/releases) и скачайте версию под вашу операционную систему:
   * **Windows**: `Antigravity.Client_1.0.14_x64_en-US.msi` или `Antigravity.Client_1.0.14_x64-setup.exe`
   * **macOS (M1/M2/M3 Apple Silicon)**: `Antigravity Client_1.0.14_aarch64.dmg`
   * **Linux**: `Antigravity.Client_1.0.14_amd64.AppImage`, `Antigravity.Client_1.0.14_amd64.deb` или `Antigravity.Client-1.0.14-1.x86_64.rpm`
2. **Запустите Клиент**: Установите и запустите приложение.
3. **Настройте IDE**: Укажите порт локального прокси `8047` в настройках плагина Antigravity или используйте автоматическое конфигурирование.

---

## 💻 Системные Требования (System Requirements)

| Операционная Система | Архитектура | Формат Дистрибутива |
| :--- | :--- | :--- |
| **Windows 10 / 11** | x64 (64-bit) | MSI Installer, Setup EXE |
| **macOS 11.0+** | Apple Silicon (aarch64), Intel (x64) | DMG (Apple Silicon) |
| **Linux (Ubuntu/Debian)** | x64 (64-bit) | DEB Package |
| **Linux (Fedora/RHEL)** | x64 (64-bit) | RPM Package |
| **Linux (Universal)** | x64 (64-bit) | AppImage |

---

## 🔍 Часто Задаваемые Вопросы (SEO & FAQ)

### Как скачать Antigravity IDE Client?
Все сборки стабильных и предварительных версий клиента публикуются во вкладке "Releases" данного публичного репозитория. Мы гарантируем подлинность дистрибутивов, собранных на нашей стороне.

### Нужна ли подписка Google AI Pro для работы клиента?
Клиент работает через Antigravity-Manager, который перенаправляет запросы к бэкенду. Для конечного пользователя нет необходимости напрямую управлять кредитами Google AI Pro — прокси автоматически авторизует ваши запросы.

### Безопасно ли использовать прокси на порту 8047?
Да, прокси-сервер работает локально на вашем компьютере (localhost) и перенаправляет запросы по защищенному протоколу HTTPS. Исходный код ядра прокси компилируется из доверенного приватного репозитория разработчиков.

---

## 📝 Лицензия (License)

Дистрибутивы и бинарные файлы Antigravity IDE Client распространяются под закрытой лицензией (Proprietary License). Исходный код ядра приложения является приватной интеллектуальной собственностью и не подлежит публичному распространению. 

---

*Разработано для максимальной продуктивности с Antigravity IDE.*
