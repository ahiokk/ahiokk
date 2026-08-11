<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg">
  <img src="assets/header-light.svg" alt="Иракли Чикобава, ML-инженер, NLP и LLM-агенты" width="100%">
</picture>

<p align="center">
  <a href="https://t.me/Ah1ok"><img src="https://img.shields.io/badge/Telegram-%40Ah1ok-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="mailto:irakli1408@yandex.ru"><img src="https://img.shields.io/badge/Почта-irakli1408-EA4335?style=for-the-badge&logo=maildotru&logoColor=white" alt="Почта"></a>
  <a href="https://leetcode.com/u/ahiok"><img src="https://img.shields.io/badge/LeetCode-ahiok-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"></a>
</p>

Занимаюсь NLP и LLM-агентами. Интереснее всего мне та часть, где агент ходит в базу, ищет по документам и заводит заявку оператору. Чистая генерация текста скучнее. Два проекта собраны целиком на локальных моделях, без единого обращения к внешним AI API.

Параллельно с учёбой работаю в рознице автозапчастей. Накладные от поставщиков там заводили руками, я написал под это desktop-приложение, и сейчас загрузка занимает пару нажатий. Оно в ежедневной работе больше года, вместе с ним живёт вторая штука, экстрактор артикулов под Ozon.

## Проекты

<table>
<tr><th align="left" width="230">Проект</th><th align="left">О чём</th><th align="left" width="270">Результат</th></tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/bank-support-ai-agent"><b>bank-support-ai-agent</b></a><br><sub>RuBERT · LLM tool calling · pgvector</sub></td>
<td valign="top">Классификация обращений клиентов банка и агент с инструментами. Уверенность классификатора работает подсказкой агенту, а не жёстким гейтом: жёсткий порог ошибочно эскалировал вопросы вроде «баланс».</td>
<td valign="top">macro-F1 <code>0.9166</code> против <code>0.8601</code> у TF-IDF и логрега.<br>Тест на 3 076 обращениях</td>
</tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/localscript-lua-agent"><b>LocalScript</b></a><br><sub>Ollama · Docker Compose · self-repair</sub></td>
<td valign="top">Локальная агентская система генерации Lua-кода, хакатон МТС True Tech 2026. Сгенерированный код проверяется через <code>luac</code>, при ошибке агент чинит сам себя и пробует снова.</td>
<td valign="top"><code>qwen2.5-coder:7b</code> локально.<br>Наружу не ходит вообще</td>
</tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/n8n-rag-telegram-bot"><b>n8n-rag-telegram-bot</b></a><br><sub>RAG · Supabase · low-code</sub></td>
<td valign="top">RAG-ассистент в Telegram по PDF из Google Drive. Переиндексация идёт по хешу файла, поэтому неизменившиеся документы не перезаливаются.</td>
<td valign="top">Supabase Vector Store, <code>topK=3</code>,<br>эмбеддинги <code>qwen3-embedding-8b</code></td>
</tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/mws-AI-agent"><b>mws-AI-agent</b></a><br><sub>Google ADK · OpenAI-совместимый API</sub></td>
<td valign="top">Ассистент подбора моделей из MWS GPT Model Hub. Диалог на Google ADK, а подбор и расчёт цены вынесены в детерминированное Python-ядро, чтобы цифры не выдумывались моделью.</td>
<td valign="top">Каталог и цены тянутся с сайта на лету</td>
</tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/russian-llm-pretrain-and-sft"><b>russian-llm-pretrain-and-sft</b></a><br><sub>BPE · pretrain · SFT</sub></td>
<td valign="top">Свой BPE-токенизатор на 16k, pretrain mini-Llama на 158.63M параметров с нуля, затем SFT Qwen2.5-0.5B на русском инструктивном датасете.</td>
<td valign="top">train loss <code>6.6133</code> → <code>1.5335</code></td>
</tr>

<tr>
<td valign="top"><a href="https://github.com/ahiokk/recsys-learning-to-rank-catboost"><b>recsys-learning-to-rank-catboost</b></a><br><sub>CatBoost · candidate generation</sub></td>
<td valign="top">Оффлайн-пайплайн ранжирования на MovieLens 20M: implicit feedback, генерация кандидатов, pointwise против learning-to-rank.</td>
<td valign="top"><code>NDCG@10 = 0.7507</code>, <code>Recall@10 = 0.966</code><br>на 1.7M кандидатов</td>
</tr>
</table>

Из соревновательного на Kaggle: 13 место в прогнозе дефицита курьеров Самоката (`WAPE 0.177` против бейзлайнов `0.563` и `0.622`) и 3 место в матчинге офферов маркетплейса на 2.5M пар (`F1 0.921` на валидации).

<details>
<summary><b>Остальные публичные репозитории</b></summary>

<br>

| Репозиторий | Что там |
|---|---|
| [fashion-clip-search](https://github.com/ahiokk/fashion-clip-search) | Дообучение CLIP под поиск fashion-товаров по тексту. Holdout CLIP score `30.45` на 44 160 парах |
| [receipt-ocr](https://github.com/ahiokk/receipt-ocr) | OCR чеков, извлечение полей и QA по документу на SROIE и локальной LLM |
| [nn_auto-completion](https://github.com/ahiokk/nn_auto-completion) | Автодополнение текста, LSTM против DistilGPT-2 |
| [gpb-deposits-liquidity-stress-test](https://github.com/ahiokk/gpb-deposits-liquidity-stress-test) | Прогноз вкладов физлиц и стресс-тест ликвидности на форме 0409806 ЦБ. `WAPE 7.5%` |
| [a101-test-task](https://github.com/ahiokk/a101-test-task) | Тестовое: Airflow и MQTT-брокер Mosquitto в одном контейнере под supervisord |
| [Dazzle](https://github.com/ahiokk/Dazzle) | Импорт накладных поставщиков в базу Tirika Shop. То самое, что в ежедневной работе |
| [avto255](https://github.com/ahiokk/avto255) | Экстрактор артикулов под Tirika и Ozon, клиентская страница без бэкенда |
| [team-finder-ad](https://github.com/ahiokk/team-finder-ad) | Django-сервис поиска участников в pet-проекты |
| [mlp_sin](https://github.com/ahiokk/mlp_sin) · [AdvancedMNISTMLP](https://github.com/ahiokk/AdvancedMNISTMLP) | Основы руками: forward и backward на голом NumPy, MLP на MNIST с логированием в ClearML |

</details>

## Стек

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Transformers">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/CatBoost-FFCC00?style=flat-square&logoColor=black" alt="CatBoost">
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas">
</p>
<p>
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama">
  <img src="https://img.shields.io/badge/RAG%20%C2%B7%20tool%20calling-6E56CF?style=flat-square" alt="RAG и tool calling">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" alt="n8n">
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white" alt="MLflow">
</p>
<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/PostgreSQL%20%2B%20pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL и pgvector">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white" alt="Airflow">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
</p>

## Учёба

**РЭУ им. Плеханова**, Высшая школа кибертехнологий, математики и статистики. 09.03.02 «Информационные системы и технологии», профиль ML-инженер, выпуск 2027.

**Яндекс.Практикум**, «Инженер по глубокому обучению нейросетей: обработка естественного языка», 260 академических часов, 2026.

**ШАД**: Agents Scaling Week 2026, LLM Scaling Week 2025.
