# 📡 ReBullet Android Scripts

## 🇬🇧 English

A set of Android scripts to **enable free mobile internet sharing** and **bypass regional restrictions** for Beeline Russia SIM cards.

---

### 🚀 Features

- 📶 **Free tethering**: Forces **TTL = 64**, so the operator doesn't detect internet sharing (hotspot)
- 🌐 Redirects all DNS requests to **Cloudflare (1.1.1.1)**
- 🌍 Overrides SIM properties to appear as **Beeline Kazakhstan**
- 🎬 Bypasses regional restrictions for apps like **TikTok**, **YouTube**, and other services
- 🧩 Fully compatible with **Magisk service.d** (runs at boot)

---

### 📦 Installation

1. ⚠️ Requires **root access** via **Magisk**
2. Open terminal and enter:

    ```sh
    su
    ```

3. Copy the scripts to:

    ```sh
    /data/adb/service.d/
    ```

4. Make them executable:

    ```sh
    chmod +x /data/adb/service.d/*.sh
    ```

5. Reboot your device. Scripts will auto-run at startup.

---

### 📁 Included Scripts

#### `change_operator.sh`
Overrides SIM country/operator to **Beeline KZ**, helping bypass geo-based restrictions.

#### `spoof_ttl_dns.sh`
- Sets TTL to 64 (prevents detection of internet sharing)
- Redirects DNS traffic to `1.1.1.1` to improve speed and bypass censorship

---

### ⚠️ Disclaimer

> **Use at your own risk.**  
> The author (ReBullet) is **not responsible** for any damage, data loss, soft-brick, or legal consequences. These scripts are provided **for educational purposes only**.

---

## 🇷🇺 Русский

Набор Android-скриптов для **бесплатной раздачи интернета** и **обхода региональных блокировок** на симкартах Beeline Россия.

---

### 🚀 Возможности

- 📶 **Бесплатная раздача интернета** — TTL устанавливается в **64**, и оператор не видит, что вы используете точку доступа (раздачу)
- 🌐 Замена системного DNS на **Cloudflare (1.1.1.1)**
- 🌍 Подмена параметров SIM-карты на **Beeline Казахстан**
- 🎬 Обход блокировок в **TikTok**, **YouTube** и других сервисах
- 🧩 Полностью совместим с **Magisk service.d** (автозапуск после перезагрузки)

---

### 📦 Установка

1. ⚠️ Необходим **рут-доступ с Magisk**
2. Откройте терминал и введите:

    ```sh
    su
    ```

3. Скопируйте скрипты в:

    ```sh
    /data/adb/service.d/
    ```

4. Сделайте их исполняемыми:

    ```sh
    chmod +x /data/adb/service.d/*.sh
    ```

5. Перезагрузите устройство — скрипты запустятся автоматически.

---

### 📁 Включённые скрипты

#### `change_operator.sh`
Меняет свойства SIM-карты, заставляя систему думать, что это **Beeline Казахстан**, для обхода геоблокировок.

#### `spoof_ttl_dns.sh`
- TTL = 64 — оператор не обнаруживает раздачу интернета
- DNS перенаправляется на `1.1.1.1` — это помогает обойти блокировки и ускорить соединение

---

### ⚠️ Дисклеймер

> **Всё используется на свой страх и риск.**  
> Автор (ReBullet) **не несёт ответственности** за любые последствия: порчу устройства, потерю данных или юридические проблемы. Скрипты предназначены **исключительно в образовательных целях**.

---
