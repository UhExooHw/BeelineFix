# ReBullet SIM Spoof

> ⚠️ **Дисклеймер:**  
> Автор скрипта **не несёт ответственности** за возможный ущерб: поломку устройства, утрату данных, сбои связи, блокировку SIM, юридические последствия и т.д.  
> Использование может нарушать условия оператора и законы вашей страны. **Всё, что вы делаете — на свой страх и риск.**
>
> Скрипт работает **только с SIM1**. Двухсимочные устройства и SIM2 **не поддерживаются**.  
> TTL spoofing не гарантирует обход всех тарифных ограничений — **используйте с осторожностью**.

---

## ⚙️ Требования

- **Android 9 (Pie, API 28) и выше**  
  (используется DoT через `private_dns_specifier`)
- **Magisk 20.4+** с поддержкой `/data/adb/service.d`
- **Root-доступ**
- **iptables** должен быть доступен в прошивке/ядре
- Для **BBR** — ядро с TCP BBR желательно, но не обязательно

---

## Что делает скрипт?

**ReBullet SIM Spoof** — установочный скрипт для Android, запускающийся через Magisk `service.d`, который позволяет:

- 🛰 **Перехватывать DNS-запросы** через iptables (обход блокировок)
- 🌍 **Подменять SIM-данные**: MCCMNC, ISO, название оператора, таймзону
- 🔒 **Устанавливать DoT (DNS-over-TLS)** через системные настройки
- 🚀 **Включать TCP BBR** — ускорение интернет-соединения (если поддерживается)
- 📶 **TTL=64 spoofing** — обход ограничений на раздачу интернета

Скрипты создаются в `/data/adb/service.d/` и автоматически запускаются при старте устройства.

---

## ✅ Поддерживаемые операторы и страны

| Оператор   | Страна     | MCCMNC  |
|------------|------------|---------|
| Beeline    | Uzbekistan | 43404   |
| Beeline    | Russia     | 25099   |
| MTS        | Belarus    | 25702   |
| MTS        | Russia     | 25001   |
| Tele2      | Russia     | 25020   |
| Tele2      | Latvia     | 24702   |
| Megafon    | Russia     | 25002   |
| Yota       | Russia     | 25011   |
| A1         | Belarus    | 25701   |
| life:)     | Belarus    | 25704   |
| Turkcell   | Turkey     | 28601   |

---

## 💻 Пример работы

```
╔════════════════════════════════════════╗
║        ReBullet SIM Spoof Utility      ║
╚════════════════════════════════════════╝

[✓] BBR is supported by the kernel.
[✓] Environment OK.

Select Mobile Operator:
  [1] Beeline        [2] MTS
  [3] Tele2 (T2)     [4] Megafon
  [5] Yota           [6] A1
  [7] life:)         [8] Turkcell

Select DNS Provider:
  [1] Cloudflare     (1.1.1.1)
  [2] Google         (8.8.8.8)
  [3] Quad9          (9.9.9.9)

[+] Creating ReBullet-SIM.sh...
[+] Creating ReBullet-TTL.sh...

[✓] Scripts successfully installed!
    /data/adb/service.d/ReBullet-SIM.sh
    /data/adb/service.d/ReBullet-TTL.sh

GitHub: https://github.com/UhExooHw/sim-spoof

Reboot required to apply changes.
  [1] Reboot now
  [2] Reboot later
```

---

## 📦 Установка

```bash
curl -s -o /data/local/tmp/spoof.sh \
  https://raw.githubusercontent.com/UhExooHw/sim-spoof/main/spoof.sh \
  && chmod +x /data/local/tmp/spoof.sh \
  && sh /data/local/tmp/spoof.sh
```

---

## 🎯 Когда пригодится?

- Если оператор **навязывает DNS**, и сайты не открываются
- Если приложения определяют **регион по SIM** (например, Google Play)
- Если оператор **вводит доплату за раздачу** — spoof TTL=64 помогает обойти ограничение

---

## 🤖 Автор

GitHub: [UhExooHw](https://github.com/UhExooHw)

---

