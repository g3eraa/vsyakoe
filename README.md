# vsyakoe

Учебные проекты по классическому машинному обучению: регрессия, классификация, кластеризация, работа с признаками, валидация моделей и т.п. Всё в Jupyter-ноутбуках на `numpy`, `pandas`, `scikit-learn`, `matplotlib` и `seaborn`.

## Структура

```
vsyakoe/
├── project1/
│   └── project_1.ipynb
├── requirements.txt   # зависимости для всех проектов
└── README.md
```

Каждый проект лежит в своей папке `projectN/` и состоит из одного или нескольких ноутбуков.

## Запуск

Нужен Python 3.12+ (проект собирался на 3.14).

### 1. Клонировать репозиторий и создать окружение

```bash
git clone <url-репозитория> vsyakoe
cd vsyakoe

python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install -r requirements.txt
```

### 2. Открыть ноутбук

**Вариант А — VS Code (удобнее всего).**
Установите расширения *Python* и *Jupyter*, откройте нужный `.ipynb`, нажмите *Select Kernel* в правом верхнем углу и выберите интерпретатор из `.venv`. После этого ячейки запускаются через `Shift+Enter` или *Run All*.

**Вариант Б — Jupyter в браузере.**
В `requirements.txt` есть только ядро (`ipykernel`), сам JupyterLab нужно поставить отдельно:

```bash
pip install jupyterlab
jupyter lab
```

Откроется браузер, дальше переходите в папку проекта и открываете ноутбук.

## Данные

Датасеты в репозиторий не коммитятся: `.gitignore` исключает `data/`, `*.csv`, `*.parquet` и т.п. Если проекту нужны внешние данные, откуда их взять и куда положить, будет написано в начале его ноутбука.
