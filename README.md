<div align="center">

# INSANE VPN

**Заметки о том, как строится VPN-сервис, который не ловится DPI**

![locations](https://img.shields.io/badge/locations-6-9146FF?style=flat-square)
![protocol](https://img.shields.io/badge/protocol-VLESS%20%2B%20Reality-c72c41?style=flat-square)
![logs](https://img.shields.io/badge/logs-none-brightgreen?style=flat-square)
![devices](https://img.shields.io/badge/devices%20per%20account-up%20to%2020-blue?style=flat-square)

[Telegram-бот](https://t.me/InsaneVPN_bot) · [Сайт](https://my.insanevpn.pro) · [Тарифы](docs/pricing.md)

</div>

---

Я управляю инфраструктурой INSANE VPN и веду этот репозиторий как инженерный дневник: как устроены системы DPI, почему одни протоколы блокируются за недели, а другие живут годами, и какие решения мы принимаем при проектировании сети.

Это не маркетинговый текст — это то, чем реально приходится думать, когда строишь сеть, которая обязана выживать под активным противодействием.

## Содержание

- [Как работает DPI](docs/dpi-deep-dive.md) — классификация трафика, active probing, TLS-фингерпринтинг, что из этого реально работает против VPN
- [Архитектура маскировки](docs/architecture.md) — почему Reality-подобные схемы живут дольше OpenVPN/IPsec, и как это реализовано у нас
- [FAQ](docs/faq.md) — частые вопросы про подключение
- [Privacy / no-logs](docs/privacy.md) — что мы храним и почему это принципиально мало
- [Тарифы](docs/pricing.md)

## Locations

| Флаг | Страна | Код |
|---|---|---|
| 🇬🇧 | United Kingdom | `UK` |
| 🇳🇱 | Netherlands | `NL` |
| 🇩🇪 | Germany | `DE` |
| 🇨🇭 | Switzerland | `CH` |
| 🇸🇪 | Sweden | `SE` |
| 🇫🇮 | Finland | `FI` |

## Почему это вообще инженерная задача

Большинство VPN-сервисов решают одну задачу — зашифровать трафик. Мы решаем другую: сделать так, чтобы зашифрованный трафик **не выглядел** как VPN-трафик. Это разные по сложности задачи, и вторая — то, что определяет, проживёт ли сервис полгода или два года.

Технические детали — в [`docs/dpi-deep-dive.md`](docs/dpi-deep-dive.md).

---

<div align="center">

Если из всего этого вам нужен не разбор протоколов, а просто рабочий VPN — [бот подключает за 2 минуты](https://t.me/InsaneVPN_bot), 1 день бесплатно.

</div>
