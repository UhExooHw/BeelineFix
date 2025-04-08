# ReBullet SIM Spoof

> ⚠️ **Дисклеймер:** Автор скрипта не несёт никакой ответственности за возможный ущерб, включая поломку устройства, утрату данных или юридические последствия, которые могут возникнуть в результате использования этого инструмента. Использование скрипта может нарушать условия обслуживания вашего мобильного оператора или законодательства вашей страны.
>
> Скрипт предназначен **только для работы с операторами Beeline и MTS**. Поддержка MTS находится в экспериментальном режиме и всё ещё тестируется.
>
> В настоящий момент скрипт **не поддерживает SIM-карты, установленные во втором слоте (SIM2)** или в конфигурациях с двумя SIM-картами. Он корректно работает **только с SIM-картой в первом слоте (SIM1)**.

SIM Spoof — это простой установочный скрипт для Android, предназначенный для работы через Magisk (через `service.d`) с автозапуском после загрузки устройства. Скрипт позволяет подменять данные SIM-карты, включая MCCMNC, ISO-код, название оператора и таймзону (timezone).

- 🛰 Перехватывает DNS-запросы через iptables, даже если оператор навязывает свой DNS  
- 🌍 Подменяет данные SIM-карты, чтобы обойти региональные ограничения  
- 🚀 Включает TCP BBR (для лучшей скорости интернета)  
- 📶 Устанавливает TTL = 64, чтобы раздавать интернет без доплат  

---

## 💻 Пример работы скрипта

```bash
========================================
         ReBullet SIM Spoof
========================================

Select Operator:
  1) Beeline
  2) MTS

Enter number (1-2): 1

Select Country:
  1) Kazakhstan (Beeline)
  2) Uzbekistan (Beeline)
  3) Russia (Beeline)

Enter number (1-3): 3

Select DNS Provider:
  1) Cloudflare (1.1.1.1)
  2) Google     (8.8.8.8)
  3) Yandex     (77.88.8.88)

Enter number (1-3): 2

[+] Creating ReBullet-SIM.sh
[+] Creating ReBullet-TTL.sh

[✓] Scripts installed:
    /data/adb/service.d/ReBullet-SIM.sh
    /data/adb/service.d/ReBullet-TTL.sh

Support the project on GitHub:
https://github.com/UhExooHw/sim-spoof

Reboot required to apply changes.
  1) Reboot now
  2) Reboot later
Choose an option (1-2): 2
Reboot manually when ready.
```

---

## 📦 Установка

```bash
curl -s -o /data/local/tmp/spoof.sh https://raw.githubusercontent.com/UhExooHw/sim-spoof/refs/heads/main/spoof.sh \
&& chmod +x /data/local/tmp/spoof.sh \
&& echo "[✓] Скрипт загружен. Запустите вручную: sh /data/local/tmp/spoof.sh"
```

---

## 🎯 Зачем это нужно?

- Если оператор **принудительно ставит свой DNS** и блокирует сайты — скрипт перехватывает трафик на уровне iptables  
- Если приложение определяет регион по **SIM-карте**  
- Если раздача Wi-Fi через смартфон **платная** — TTL=64 помогает скрыть tethering  

---
```