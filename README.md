<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg">
  <img src="assets/header-light.svg" alt="Иракли Чикобава, AI/NLP-инженер" width="100%">
</picture>

<p align="center">
  <a href="https://t.me/Ah1ok"><img src="https://img.shields.io/badge/Telegram-%40Ah1ok-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="mailto:irakli1408@yandex.ru"><img src="https://img.shields.io/badge/Почта-irakli1408-EA4335?style=for-the-badge&logo=maildotru&logoColor=white" alt="Почта"></a>
  <a href="https://leetcode.com/u/ahiok"><img src="https://img.shields.io/badge/LeetCode-ahiok-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"></a>
</p>

Студент РЭУ им. Плеханова, «Информационные системы и технологии», выпуск 2027. Москва.

Работаю с NLP и LLM: дообучение трансформеров под классификацию, агенты с вызовом инструментов, RAG поверх векторных баз, обучение языковых моделей с нуля. Вне учёбы пишу автоматизацию для розницы автозапчастей, два инструмента в ежедневной эксплуатации.

## Стек

| | |
|---|---|
| **Языки** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL"> <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" alt="Bash"> |
| **ML и DL** | <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch"> <img src="https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Transformers"> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn"> <img src="https://img.shields.io/badge/CatBoost-FFCC00?style=flat-square&logoColor=black" alt="CatBoost"> <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas"> |
| **LLM и агенты** | <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama"> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain"> <img src="https://img.shields.io/badge/RAG-6E56CF?style=flat-square" alt="RAG"> <img src="https://img.shields.io/badge/tool%20calling-6E56CF?style=flat-square" alt="tool calling"> <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" alt="n8n"> |
| **Хранилища** | <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square" alt="pgvector"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> |
| **Инфраструктура** | <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white" alt="Airflow"> <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white" alt="MLflow"> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git"> |

## Проекты

| Проект | Задача | Стек | Результат |
|---|---|---|---|
| [**bank-support-ai-agent**](https://github.com/ahiokk/bank-support-ai-agent) | Классификация обращений клиентов банка и агент, который по интенту вызывает инструменты: счёт и транзакции из Postgres, поиск по базе знаний, эскалация оператору | RuBERT, PyTorch, PostgreSQL + pgvector, Chainlit, MLflow | macro-F1 `0.9166` против `0.8601` у TF-IDF и логрега, тест на 3 076 обращениях |
| [**localscript-lua-agent**](https://github.com/ahiokk/localscript-lua-agent) | Агентская система генерации Lua-кода. Результат валидируется через `luac`, при ошибке компиляции агент чинит код и повторяет попытку | Ollama, `qwen2.5-coder:7b`, FastAPI, Docker Compose | Хакатон МТС True Tech 2026. Работает без обращений к внешним AI API |
| [**russian-llm-pretrain-and-sft**](https://github.com/ahiokk/russian-llm-pretrain-and-sft) | Обучение языковой модели с нуля: свой BPE-токенизатор на 16k, pretrain mini-Llama на 158.63M параметров, затем SFT Qwen2.5-0.5B | PyTorch, Transformers, trl | train loss `6.6133` → `1.5335` |
| [**mws-AI-agent**](https://github.com/ahiokk/mws-AI-agent) | Подбор модели из MWS GPT Model Hub под сценарий и бюджет. Диалог на LLM, подбор и расчёт стоимости на детерминированном ядре | Google ADK, FastAPI, OpenAI-совместимый API | Каталог и цены загружаются с сайта в рантайме |
| [**n8n-rag-telegram-bot**](https://github.com/ahiokk/n8n-rag-telegram-bot) | RAG-ассистент в Telegram по PDF из Google Drive. Переиндексация по хешу файла, ответы только по найденным фрагментам | n8n, Supabase Vector Store, `qwen3-embedding-8b` | `topK=3`, индексация и ответы в одном workflow |
| [**recsys-learning-to-rank-catboost**](https://github.com/ahiokk/recsys-learning-to-rank-catboost) | Оффлайн-пайплайн ранжирования: implicit feedback, генерация кандидатов, сравнение pointwise и learning-to-rank | CatBoost, scikit-learn, pandas | `NDCG@10 = 0.7507`, `Recall@10 = 0.966` на 1.7M кандидатов |
| [**fashion-clip-search**](https://github.com/ahiokk/fashion-clip-search) | Дообучение CLIP под поиск товаров по текстовому запросу, от подготовки данных до retrieval-выдачи | PyTorch, Transformers, CLIP | holdout CLIP score `30.45` на 44 160 парах |
| [**receipt-ocr**](https://github.com/ahiokk/receipt-ocr) | OCR чеков, извлечение структурированных полей и ответ на вопрос по документу | pytesseract, локальная LLM, PyTorch | MVP на датасете SROIE |
| [**gpb-deposits-liquidity-stress-test**](https://github.com/ahiokk/gpb-deposits-liquidity-stress-test) | Прогноз вкладов физлиц и стресс-тест ликвидности на публичной отчётности ЦБ, форма 0409806 | pandas, statsmodels, BeautifulSoup | `WAPE 7.5%` на отложенных 4 кварталах |
| [**nn_auto-completion**](https://github.com/ahiokk/nn_auto-completion) | Автодополнение текста: LSTM против DistilGPT-2 на одной задаче в разных постановках | PyTorch, Transformers | 1.28M обучающих примеров |

## Соревнования

| Соревнование | Задача | Метрика | Место |
|---|---|---|---|
| Матчинг офферов маркетплейса | Бинарная классификация 2.5M пар на NLP- и CV-эмбеддингах | `F1 0.921` на валидации, `0.93985` на LB при лидере `0.94528` | **3** |
| Прогноз дефицита курьеров Самоката | Регрессия на неделю вперёд | `WAPE 0.177`, бейзлайны `0.563` и `0.622` | **13** |
| Классификация классов звёзд | Multiclass на табличных данных | `balanced accuracy 0.96576` при лидере `0.97283` | 809 |

## Автоматизация в проде

Розница автозапчастей, инструменты написаны по своей инициативе и используются ежедневно.

| Инструмент | Что делает |
|---|---|
| [**Dazzle**](https://github.com/ahiokk/Dazzle) | Импорт накладных поставщиков в базу Tirika Shop. Матчинг по артикулам, кросс-кодам и штрихкодам, предпросмотр, ручная корректировка, резервное копирование перед записью. Заведение накладной сократилось до пары нажатий |
| [**avto255**](https://github.com/ahiokk/avto255) | Экстрактор артикулов под Tirika и Ozon. Чистит вставленный список, убирает дубликаты, отдаёт готовый набор. Обработка 100 позиций с пяти минут до секунд |

## Ещё в профиле

[**a101-test-task**](https://github.com/ahiokk/a101-test-task) — Airflow и MQTT-брокер Mosquitto в одном контейнере под supervisord.
[**team-finder-ad**](https://github.com/ahiokk/team-finder-ad) — Django-сервис поиска участников в pet-проекты, PostgreSQL в docker compose, автотесты.
[**mlp_sin**](https://github.com/ahiokk/mlp_sin) и [**AdvancedMNISTMLP**](https://github.com/ahiokk/AdvancedMNISTMLP) — forward и backward на голом NumPy, MLP на MNIST с логированием в ClearML.

## Образование

**РЭУ им. Плеханова**, Высшая школа кибертехнологий, математики и статистики. 09.03.02 «Информационные системы и технологии», выпуск 2027.

**Яндекс.Практикум** — «Инженер по глубокому обучению нейросетей: обработка естественного языка», 260 академических часов, 2026.

**ШАД** — Agents Scaling Week 2026, LLM Scaling Week 2025.
