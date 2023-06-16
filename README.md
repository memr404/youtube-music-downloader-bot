# youtube-music-downloader-bot

Данный код представляет собой бота для загрузки музыки из Ютуба, написанного на Python. Он использует библиотеку `aiogram` для функциональности Telegram-бота и `pytube` для загрузки видео и плейлистов с YouTube. Загруженная музыка сохраняется в формате MP3 и может быть доступна через бота.

## Предварительная настройка

Перед запуском кода убедитесь, что у вас установлены следующие зависимости:

- `aiogram`
- `pytube`
- `eyed3`
- `ffmpeg`

Вы можете установить эти зависимости с помощью `pip`:

```bash
pip install aiogram pytube eyed3
```

`ffmpeg` необходим для конвертации загруженных видео в формат MP3. Вы можете установить его, следуя инструкциям для вашей операционной системы.

## Настройка

1. Клонируйте репозиторий или загрузите файлы кода.

2. Создайте нового Telegram-бота и получите его API-токен. Вы можете сделать это, обратившись к BotFather в Telegram.

3. Откройте файл с кодом и замените переменную `token` на свой API-токен Telegram-бота:

   ```python
   token = 'ВАШ_ТОКЕН'
   ```

4. Запустите код с помощью интерпретатора Python:

   ```bash
   python main.py
   ```

## Использование

После запуска бота вы можете взаимодействовать с ним через Telegram. Вот доступные команды:

- `/start`: Запустить бота и инициализировать необходимую базу данных и каталоги.
- `/get` или "📂Показать всю скаченную музыку": Получить список всех загруженных песен.
- `/clear`: Удалить все загруженные песни.
- `/help`: Получить справку и инструкции по использованию.

Для загрузки музыки отправьте боту ссылку на видео или плейлист YouTube. Бот начнет загрузку аудио в формате MP3. Если вы отправите плейлист, бот загрузит все песни из плейлиста.

Загруженные песни можно просмотреть, выбрав опцию "📂Показать всю скаченную музыку". Чтобы прослушать песни, отправьте ответом на сообщение "1!" и бот отправит аудиофайлы.

Чтобы удалить все загруженные песни, используйте команду `/clear`.

## Примечания

- Загруженные песни сохраняются в каталоге с именем идентификатора чата пользователя. После отправки пользователю, они удаляются с локального сервера. ID файла храниться в файле `ids.txt`
- Бот использует SQLite для хранения информации о пользователях, включая идентификатор чата и имя пользователя.
- Библиотека `eyed3` используется для добавления метаданных (названия песни и исполнителя) в загруженные файлы MP3.
- Утилита `ffmpeg` используется для конвертации загруженных видео в формат MP3.

Не стесняйтесь настраивать код в соответствии с вашими требованиями или добавлять дополнительные функции в бота. Наслаждайтесь загрузкой и прослушиванием любимой музыки!
