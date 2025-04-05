# 📱 ReBullet SIM Spoof

> Мощный Android-скрипт для подмены страны SIM-карты, TTL, DNS и активации BBR через Magisk

---

## ✨ Преимущества

- 🌍 **Подмена страны SIM-карты**
  - MCC/MNC, ISO-код, отображение Beeline
  - Обход региональных ограничений в приложениях

- 📶 **TTL Spoofing**
  - Установка TTL = 64
  - Позволяет бесплатно раздавать интернет, если оператор ограничивает

- 🌐 **Подмена DNS**
  - Выбор между Cloudflare, Google и Yandex DNS
  - Полный контроль над DNS-запросами (перехват через iptables)

- ⚡ **Активация TCP BBR**
  - Повышение скорости интернета и стабильности

- 🧠 **Обход геоблокировок**
  - Приложения, определяющие регион по SIM, будут считать что вы в другой стране

---

## ⚙️ Требования

- Android с root-доступом
- Magisk установлен
- Ядро с поддержкой TCP BBR
- iptables

---

## 🚀 Установка

```bash
chmod +x rebullet.sh
./rebullet.sh
```

После запуска выберите страну, DNS и подтвердите установку.  
Скрипты `ReBullet-SIM.sh` и `ReBullet-TTL.sh` будут установлены в `/data/adb/service.d/` и автоматически применяться при каждой загрузке.

---

## 🖥 Пример вывода скрипта

```text
======================================
         ReBullet SIM Spoof
======================================
Magisk is installed
Kernel supports BBR, continuing...

Select Country:
  1) Kazakhstan
  2) Uzbekistan
  3) Russia
Enter number (1-3): 1

Select DNS Provider:
  1) Cloudflare (1.1.1.1)
  2) Google (8.8.8.8)
  3) Yandex (77.88.8.88)
Enter number (1-3): 1

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
Choose an option (1-2):
```

---

## ⚠️ Дисклеймер

**Автор не несёт никакой юридической ответственности** за использование скрипта.  
Использование может нарушать условия оператора или законы вашей страны.  
Скрипт предоставляется исключительно в **образовательных и исследовательских целях**.  
Всю ответственность за действия несёт пользователь.

---

## 💡 Примеры использования

- Обход блокировок YouTube, TikTok, Instagram и других сервисов
- Раздача мобильного интернета без ограничения
- Защита DNS-запросов от подмены оператором
- Ускорение соединения в сетях 4G/5G

---

## 👨‍💻 Автор

**ReBullet**  
GitHub: [UhExooHw](https://github.com/UhExooHw/sim-spoof)

---

## ⭐ Поддержка проекта

Поставьте звезду ⭐️ на GitHub, если скрипт вам полезен!
