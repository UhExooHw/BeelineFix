---

# **ReBullet SIM Spoof**

> ⚠️ **Дисклеймер:**  
> Автор скрипта **не несёт ответственности** за любой возможный ущерб: поломку устройства, утрату данных, сбои связи, блокировки SIM-карты, юридические последствия и т.д.  
> Использование может нарушать условия оператора и законы вашей страны. **Всё, что вы делаете — на свой страх и риск.**
>
> Скрипт работает **только с SIM1**. Двухсимочные устройства и SIM2 **не поддерживаются**.  
> TTL spoofing не гарантирует обход всех тарифных ограничений — **используйте с осторожностью**.

---

## **Что делает этот скрипт?**

**ReBullet SIM Spoof** — это установочный скрипт для Android с Magisk, который позволяет:

- 🛰 **Перехватывать DNS-запросы** через iptables (обход блокировок)
- 🌍 **Подменять SIM-данные**: MCCMNC, ISO, название оператора и часовой пояс
- 🚀 **Включать TCP BBR** — для ускорения интернета
- 📶 **Устанавливать TTL=64** — для обхода ограничений раздачи интернета

Работает через `/data/adb/service.d` и запускается автоматически при старте системы.

---

## ✅ **Поддерживаемые операторы и страны**

| Оператор   | Страна     | MCCMNC  |
|------------|------------|---------|
| Beeline    | Uzbekistan | `43404` |
| Beeline    | Russia     | `25099` |
| MTS        | Belarus    | `25702` |
| MTS        | Russia     | `25001` |
| Tele2      | Russia     | `25020` |
| Tele2      | Latvia     | `24702` |
| Megafon    | Russia     | `25002` |
| Yota       | Russia     | `25011` |
| A1         | Belarus    | `25701` |
| life:)     | Belarus    | `25704` |
| Turkcell   | Turkey     | `28601` |

---

## 💻 **Пример работы скрипта**

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
  [3] Yandex         (77.88.8.88)
  [4] Quad9          (9.9.9.9)

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

## 📦 **Установка**

```bash
curl -s -o /data/local/tmp/spoof.sh https://raw.githubusercontent.com/UhExooHw/sim-spoof/main/spoof.sh \
&& chmod +x /data/local/tmp/spoof.sh \
&& sh /data/local/tmp/spoof.sh
```

---

## 🎯 **Когда это пригодится?**

- Если оператор **принудительно навязывает DNS**, и сайты не открываются  
- Если приложения определяют **регион по SIM-карте** (например, Google Play, стриминг)  
- Если оператор **вводит доплату за раздачу** — spoof TTL=64 помогает обойти ограничение  

---