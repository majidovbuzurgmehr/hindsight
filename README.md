# Hindsight

**English** · [Русский](#русский)

> A private memory for your Mac. Hindsight quietly remembers what appeared on your screen, so you can find any message, number, link or error you saw — days or weeks later.

[**⬇ Download the latest version**](https://github.com/majidovbuzurgmehr/hindsight/releases/latest) · macOS 26 or later · Apple Silicon (M1 and newer)

---

## What is Hindsight?

You read something important — a message in a chat, an order number, a line of code, an address — and later you can't remember where it was. Hindsight solves that. It lives in the notch of your MacBook (like a Dynamic Island), records your screen in the background, reads the text on it, and lets you search everything you've seen in an instant.

**Everything stays on your Mac.** There are no accounts, no servers and no analytics.

## What it can do

- **Instant search** across everything that appeared on your screen — works with Russian and English, finds partial words, and understands meaning, not just exact words. Press **⌥ Space** from anywhere.
- **Timeline** — scroll back through your day like a video and jump to the exact moment a search result came from, with the found text highlighted.
- **Ask** — ask questions in plain language ("What was the order number yesterday?") and get an answer with links to the exact moments it came from. Answers are generated **on your Mac** by Apple Intelligence (if your Mac supports it) or by a local model you can download (Qwen3). The local models understand Russian.
- **Daily summary** — what you worked on, in which apps, and for how long.
- **Privacy Center** — choose apps, windows and websites that must never be recorded, skip private browser windows, delete the last 15 minutes / hour / day / everything, and lock your history behind Touch ID or your password.
- **Pause anytime** with **⌃ ⌥ P** or from the notch.
- Lightweight by design: it saves a frame only when the screen actually changes, reads text only when you're not typing, and slows down on battery, in Low Power Mode, or when the Mac is hot.

## Privacy and security

Hindsight is built around one rule: **your screen history never leaves your Mac.**

- Screenshots are stored **encrypted** (AES-GCM) and the text database is encrypted with SQLCipher. The key lives in your macOS Keychain.
- Text recognition (OCR), search, and AI answers all run **on-device**.
- Password fields are never read. Excluded apps are cut out of the capture by macOS itself, so their windows never reach Hindsight.
- The only network connections the app ever makes:
  1. **Update checks** (via Sparkle) — they send no personal data and can be turned off in Settings.
  2. **Downloading an answer model** from Hugging Face — only if you press "Download", and it sends nothing but the names of the files.
- History is kept for 30 days by default (configurable) and old data is removed automatically.
- You can delete everything, or uninstall the app together with all its data, from Settings.

> ⚠️ Hindsight records everything visible on your screen, including things you may not want stored. Use the Privacy Center to exclude sensitive apps and websites, and only use Hindsight on a Mac you own. You are responsible for complying with the laws and agreements that apply to you (for example, when screen content includes other people's information).

## Requirements

- A Mac with **Apple Silicon** (M1 or newer). Intel Macs are not supported.
- **macOS 26** or later.
- About 100–150 MB of memory while recording. While answering a question, a local model temporarily needs about 3–4 GB (the smaller model needs about 1.5 GB); it is unloaded after a couple of idle minutes.
- Free disk space for history (limit configurable, 20 GB by default).

## Installation

1. Download the **`Hindsight-x.y.dmg`** file from the [Releases page](https://github.com/majidovbuzurgmehr/hindsight/releases/latest).
2. Open it and drag **Hindsight** into **Applications**.
3. Launch Hindsight and follow the short welcome guide.

The app is signed with an Apple Developer ID and **notarized by Apple**, so macOS opens it without scary warnings.

### Permissions

| Permission | Needed? | Why |
|---|---|---|
| **Screen & System Audio Recording** | Required | So Hindsight can see your screen. macOS shows its recording indicator while this is on. |
| **Accessibility** | Optional | Reads text straight from apps — more accurate and lighter than recognizing it from pixels. Without it, Hindsight uses OCR only. |
| **Automation (browsers)** | Optional | Saves the page address so a search result can reopen the page, and detects private windows. macOS asks once per browser. |

After allowing Screen Recording in System Settings, macOS may ask you to reopen Hindsight.

## Updates

Hindsight can update itself. Updates are signed and verified before installation. You can check manually or turn automatic checks off in **Settings → General → Updates**.

## Uninstall

**Settings → General → Uninstall…** removes the app, all recordings, the text database, the encryption key and settings, and moves the app to the Trash.

## Known limitations

- Private windows in Safari are not detected reliably; Chrome-based browsers are detected via Automation. Use website/title rules in the Privacy Center for extra safety.
- Apple Intelligence does not support Russian yet — for Russian answers use the downloadable local model.
- The source code is not published.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/majidovbuzurgmehr/hindsight/issues). Please don't attach screenshots or text from your history.

---

<a name="русский"></a>

# Hindsight — по-русски

[English](#hindsight) · **Русский**

> Личная память вашего Mac. Hindsight тихо запоминает всё, что появлялось на экране, чтобы вы могли найти любое сообщение, номер, ссылку или ошибку — через дни и недели.

[**⬇ Скачать последнюю версию**](https://github.com/majidovbuzurgmehr/hindsight/releases/latest) · macOS 26 и новее · Apple Silicon (M1 и новее)

---

## Что это такое

Вы прочитали что-то важное — сообщение в чате, номер заказа, строчку кода, адрес — а потом не можете вспомнить, где это было. Hindsight решает эту проблему. Он живёт в «чёлке» MacBook (как Dynamic Island), в фоне записывает экран, читает текст на нём и позволяет мгновенно искать по всему, что вы видели.

**Всё остаётся на вашем Mac.** Никаких аккаунтов, серверов и аналитики.

## Что умеет

- **Мгновенный поиск** по всему, что было на экране: русский и английский, неполные слова, поиск по смыслу, а не только по точным словам. Вызов откуда угодно: **⌥ Пробел**.
- **Таймлайн** — прокручивайте свой день как видео и переходите к тому самому моменту, где был найден текст, с подсветкой найденных слов.
- **Ask (вопросы)** — задавайте вопросы обычным языком («Какой был номер заказа вчера?») и получайте ответ со ссылками на конкретные моменты. Ответы создаются **на вашем Mac**: через Apple Intelligence (если ваш Mac его поддерживает) или через локальную модель, которую можно скачать (Qwen3). Локальные модели понимают русский.
- **Итоги дня** — над чем вы работали, в каких приложениях и сколько времени.
- **Центр приватности** — выбирайте приложения, окна и сайты, которые нельзя записывать, пропускайте приватные окна браузеров, удаляйте последние 15 минут / час / день / всё, защищайте историю Touch ID или паролем.
- **Пауза в любой момент**: **⌃ ⌥ P** или из «чёлки».
- Экономичность: кадр сохраняется только если экран действительно изменился, текст читается, когда вы не печатаете, а на батарее, в режиме энергосбережения или при нагреве приложение работает медленнее.

## Приватность и безопасность

Главное правило Hindsight: **история вашего экрана не покидает ваш Mac.**

- Скриншоты хранятся **в зашифрованном виде** (AES-GCM), база текста зашифрована через SQLCipher. Ключ лежит в связке ключей macOS.
- Распознавание текста (OCR), поиск и ответы ИИ выполняются **на устройстве**.
- Поля паролей не читаются. Исключённые приложения вырезаются из записи самой macOS, их окна вообще не попадают в Hindsight.
- Единственные обращения приложения в интернет:
  1. **Проверка обновлений** (через Sparkle) — не отправляет личных данных и отключается в настройках.
  2. **Скачивание модели для ответов** с Hugging Face — только если вы нажали «Скачать»; отправляются лишь названия файлов.
- История хранится по умолчанию 30 дней (настраивается), старые данные удаляются автоматически.
- В настройках можно удалить всю историю или удалить приложение вместе со всеми данными.

> ⚠️ Hindsight записывает всё, что видно на экране, в том числе то, что вы, возможно, не хотели бы хранить. Используйте Центр приватности, чтобы исключить чувствительные приложения и сайты, и пользуйтесь Hindsight только на своём Mac. Вы сами отвечаете за соблюдение законов и соглашений, которые к вам применимы (например, когда на экране есть чужая информация).

## Требования

- Mac на **Apple Silicon** (M1 и новее). Mac на процессорах Intel не поддерживаются.
- **macOS 26** и новее.
- Около 100–150 МБ памяти во время записи. Пока модель отвечает на вопрос, ей временно нужно около 3–4 ГБ (меньшей модели около 1,5 ГБ); через пару минут простоя она выгружается.
- Свободное место на диске для истории (лимит настраивается, по умолчанию 20 ГБ).

## Установка

1. Скачайте файл **`Hindsight-x.y.dmg`** на [странице релизов](https://github.com/majidovbuzurgmehr/hindsight/releases/latest).
2. Откройте его и перетащите **Hindsight** в папку **Программы**.
3. Запустите Hindsight и пройдите короткое приветствие.

Приложение подписано сертификатом Apple Developer ID и **нотаризовано Apple**, поэтому macOS открывает его без пугающих предупреждений.

### Разрешения

| Разрешение | Нужно? | Зачем |
|---|---|---|
| **Запись экрана и системного звука** | Обязательно | Чтобы Hindsight видел ваш экран. Пока оно включено, macOS показывает индикатор записи. |
| **Универсальный доступ** | По желанию | Читает текст прямо из приложений — точнее и легче, чем распознавание по картинке. Без него используется только OCR. |
| **Автоматизация (браузеры)** | По желанию | Сохраняет адрес страницы, чтобы из результата поиска можно было открыть её снова, и определяет приватные окна. macOS спросит один раз для каждого браузера. |

После разрешения записи экрана в Системных настройках macOS может предложить перезапустить Hindsight.

## Обновления

Hindsight умеет обновляться сам. Обновления подписаны и проверяются перед установкой. Проверять можно вручную, а автоматическую проверку можно отключить в **Настройки → Основные → Обновления**.

## Удаление

**Настройки → Основные → Удалить…** удаляет приложение, все записи, текстовую базу, ключ шифрования и настройки, а само приложение переносит в Корзину.

## Известные ограничения

- Приватные окна Safari определяются ненадёжно; браузеры на основе Chrome определяются через «Автоматизацию». Для надёжности используйте правила по сайтам и заголовкам окон в Центре приватности.
- Apple Intelligence пока не поддерживает русский язык — для ответов на русском используйте скачиваемую локальную модель.
- Исходный код не опубликован.

## Обратная связь

Нашли ошибку или есть идея? [Создайте обращение](https://github.com/majidovbuzurgmehr/hindsight/issues). Пожалуйста, не прикладывайте скриншоты и текст из вашей истории.
