# 🚀 ReBullet SIM Spoof Utility

> ⚠️ **Внимание:** Использование скрипта может нарушать законы или условия оператора. Всё — **на ваш страх и риск**.  
> ⚠️ Работает **только с SIM1**. SIM2 не поддерживается.

---

## ⚙️ Требования

- Android 9+ (API 28)
- Magisk 20.4+
- iptables
- Ядро с TCP BBR (опционально)

---

## 💡 Возможности

- 🌍 Подмена SIM: MCCMNC, ISO оператора
- 🕓 Подмена часового пояса
- 🔐 Перехват DNS и DoT (DNS over TLS) (IPv4/IPv6)
- 🚀 Активация TCP BBR
- 📶 TTL=64 spoof
- ⚠️ Обход геоблокировок в сервисах, определяющих страну по SIM-карте (Google Play, TikTok и др.)

---

## 🌐 Поддержка операторов

| Оператор     | Страна         | MCCMNC |
|--------------|----------------|--------|
| Beeline      | Uzbekistan     | 43404  |
| Beeline      | Kazakhstan     | 40101  |
| Beeline      | Russia         | 25099  |
| MTS          | Belarus        | 25702  |
| MTS          | Russia         | 25001  |
| t2           | Russia         | 25020  |
| Tele2        | Latvia         | 24702  |
| Tele2        | Sweden         | 24007  |
| Tele2        | Estonia        | 24803  |
| Megafon      | Russia         | 25002  |
| Yota         | Russia         | 25011  |
| A1           | Belarus        | 25701  |
| life:)       | Belarus        | 25704  |
| Salt         | Switzerland    | 22803  |
| Turkcell     | Turkey         | 28601  |
| Telia        | Finland        | 24491  |
| Telekom      | Germany        | 26201  |
| KPN          | Netherlands    | 20408  |

---

## 📦 Установка

```bash
rm -f /data/local/tmp/spoof.sh && \
curl -fsSL -o /data/local/tmp/spoof.sh https://raw.githubusercontent.com/UhExooHw/sim-spoof/main/spoof.sh && \
chmod +x /data/local/tmp/spoof.sh && \
sh /data/local/tmp/spoof.sh
```

---

## 🖥 Пример вывода

```
╔════════════════════════════════════════╗
║        ReBullet SIM Spoof Utility      ║
╚════════════════════════════════════════╝

[•] Checking environment...
[✓] BBR is supported by the kernel.
[✓] Environment OK.

Select Mobile Operator:
  [1] Beeline
  [2] MTS
  [3] Tele2 (T2)
  [4] Megafon (Russia)
  [5] Yota (Russia)
  [6] A1 (Belarus)
  [7] life:) (Belarus)
  [8] Salt (Switzerland)
  [9] Turkcell (Turkey)
  [10] Telia (Finland)
  [11] Telekom (Germany)
  [12] KPN (Netherlands)
  [13] Custom (manual input)
  [0] Exit
Enter number (0-13): 13

Manual Custom Input:
MCCMNC: 25099
ISO (e.g. ru): ru
TimeZone (e.g. Europe/Moscow): Europe/Moscow
Operator Name: Beeline

Choose DNS Provider:
  [1] Cloudflare (1.1.1.1)
  [2] Google     (8.8.8.8)
  [3] Quad9      (9.9.9.9)
  [4] Custom DNS
  [0] Back
Enter number (0-4): 4

Enter DNS IP: 1.1.1.1
Enter DoT hostname: one.one.one.one

[+] Creating ReBullet-SIM.sh...
[+] Creating ReBullet-TTL.sh...

╔══════════════════════════════════════════╗
║   [✓] Scripts successfully installed!    ║
║   Loaded on boot via Magisk service.d    ║
╚══════════════════════════════════════════╝

Location: /data/adb/service.d/ReBullet-*.sh

GitHub: https://github.com/UhExooHw/sim-spoof

Reboot required to apply changes.
  [1] Reboot now
  [2] Reboot later
Choose an option (1-2): 2
You can reboot manually later.

```

---

## 👤 Автор

GitHub: [UhExooHw](https://github.com/UhExooHw)
