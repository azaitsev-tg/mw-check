# Service Report — MyWellness NetCheck (`v2.0.0`)

Автономный браузерный инструмент для проверки сетевой доступности сервисов **Technogym MyWellness** на консолях **Technogym Live (Android)** и смартфонах в сети фитнес-клуба.

## Возможности `v2.0.0`

- Проверка **41 узла**, сверенного с эталонным *Technogym Service Platform — Network Analyzer* (включая `/robots.txt`, `/say33`, `/api/v1/status`, `ai-api.mywellness.com`, `worldweatheronline.com`).
- Автоматическое определение **GeoIP-локации**, внешнего IP, провайдера (ISP) и часового пояса устройства.
- **Передача отчёта с консоли тренажёра по QR-коду** (автономная генерация через локальный `vendor/qrcode.js`, без внешних CDN):
  - *Ссылка на телефон (`#r=...`)* — компактный QR-код; при сканировании открывает расшифрованный отчёт на смартфоне с кнопкой **«Поделиться»** (Telegram / WhatsApp / почта).
  - *Компактный текст (офлайн)* — сводка с короткими числовыми кодами `#01`–`#41` недоступных узлов (`TO` / `FL`).
- **Умный диагноз + мини-гайд** с переключением вкладок **«Для сотрудника клуба»** / **«Для IT-специалиста»** и сворачиваемым полным чеклистом проверок.

## Справочник кодов узлов (для офлайн-QR)

| Код | Узел | Код | Узел |
|---:|---|---:|---|
| `#01` | `www.mywellness.com/robots.txt` | `#22` | `meet.mywellness.com` |
| `#02` | `account.mywellness.com` | `#23` | `oid.mywellness.com` |
| `#03` | `achievement.mywellness.com` | `#24` | `pay.mywellness.com` |
| `#04` | `ai-api.mywellness.com` | `#25` | `races.mywellness.com` |
| `#05` | `api.mywellness.com` | `#26` | `reporting.mywellness.com` |
| `#06` | `api-exerp.mywellness.com` | `#27` | `services.mywellness.com` |
| `#07` | `assessment.mywellness.com` | `#28` | `storeapi.mywellness.com` |
| `#08` | `booking.mywellness.com/say33` | `#29` | `training.mywellness.com` |
| `#09` | `calendar.mywellness.com` | `#30` | `ud.mywellness.com` |
| `#10` | `challenges.mywellness.com` | `#31` | `workout.mywellness.com` |
| `#11` | `cms.mywellness.com` | `#32` | `workout.mywellness.com/say33` |
| `#12` | `coach.mywellness.com` *(опц.)* | `#33` | `onedevice-api.technogym.com/api/v1/status` |
| `#13` | `comm.mywellness.com` | `#34` | `www.technogym.com` |
| `#14` | `contentrelease.mywellness.com` *(опц.)* | `#35` | `www.worldweatheronline.com` |
| `#15` | `core.mywellness.com` | `#36` | `google.com` |
| `#16` | `core.mywellness.com/say33` | `#37` | `googleapis.com` |
| `#17` | `eam.mywellness.com` | `#38` | `google-analytics.com` *(опц.)* |
| `#18` | `eam-api.mywellness.com` | `#39` | `facebook.com` *(опц.)* |
| `#19` | `fuse.mywellness.com` | `#40` | `fbcdn.net` *(опц.)* |
| `#20` | `iotcore.mywellness.com` | `#41` | `amazonaws.com` *(опц.)* |
| `#21` | `leaderboards.mywellness.com` | | |