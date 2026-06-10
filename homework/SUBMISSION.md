# Submission

Заполните файл перед отправкой PR.

## Ссылка на репозиторий с заданием

- Repo URL: `https://github.com/margogs/rag-project-gasparova`

## Автор

- Гаспарова Маргарита Сергеевна / ник: `margogs`

## Комментарий

Учебный RAG: подбор витаминных «шотов» по текстовому запросу.
Прикладной контекст — ИИ-бот для вендингового автомата «микс ит».

- **Данные:** NIH Dietary Supplement Label Database (DSLD), публичный API,
  лицензия CC0. Собрано 1500 этикеток шотов → 4943 чанка после нарезки.
- **Pipeline:** данные (`scripts/fetch_data.py`) → ingest → chunking → TF-IDF индекс →
  retrieval (cosine top-k) → demo-ответ с источниками → Streamlit UI.
- **Поведение:** ответ строго по найденным чанкам с показом `doc_id` и score;
  при отсутствии данных — честный отказ.
