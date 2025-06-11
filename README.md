# AI Social Auto-Posting 

Автоматизированный сценарий публикации контента (текста + изображения)  
в VK • Telegram • Facebook на базе Make + OpenAI

## Описание проекта

Этот проект решает задачу «быстрого» выпуска тематического контента в соцсетях.  
Вы просто вносите в Google Sheets новую строку с **темой поста**, а система:

1. Генерирует текст через GPT-4o (ChatGPT).  
2. Создаёт иллюстрацию через DALL·E 3.  
3. Публикует пост в:
   - ВКонтакте (от имени администратора)
   - Telegram-канал (бот)
   - Facebook-страницу

Весь процесс полностью автоматизирован на платформе Make (Integromat).

## Основные функции

- **Триггер**: Google Sheets → Watch New Rows  
- **Генерация текста**: OpenAI GPT-4o  
- **Генерация картинки**: OpenAI DALL·E 3  
- **Роутер**: Make → три ветки публикации  
- **VK API**:  
  1. photos.getWallUploadServer  
  2. Upload (multipart/form-data)  
  3. photos.saveWallPhoto  
  4. wall.post  
- **Telegram Bot API**: sendPhoto + sendMessage  
- **Facebook Graph API**: page/photos → пост

## Структура репозитория

```text
├── README.md                    
├── blueprint.json            
├── Коммерческое предложение.docx  
├── img/                          
└── .gitignore
```

## Планы на будущее

- Добавить LinkedIn и X (Twitter)  
- Интегрировать Whisper/TTS для голосовых постов  
- Собирать статистику (BigQuery, Metabase)  

## Лицензия

Этот проект создан в учебных целях.  
При коммерческом использовании — обратитесь к автору за условиями.
