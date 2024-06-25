## Подробное описание на Kaggle.сom: <br>
[House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview)<br>

## Данные
Наблюдения: &nbsp; 1460 строк. <br>

Признаки: &nbsp;  80 колонок (_float64(3), int64(34), object(43)_). <br>

Целевой признак: &nbsp; количественный, _int64_.

## Решение

### Предобработка данных:
- пропущенные значения: &nbsp; `SimpleImputer()`, `pd.fillna()`;
- категориальные признаки: &nbsp; `OrdinalEncoder()`, `pd.get_dummies()`.

### Оптимизация данных:
- удаление заведомо незначимых колонок;
- удаление неинформативных колонок с большим количеством пропусков;
- Выявление аномальных значений;
- Выявление и фильтрация категорий, не встречающихся в тестовых данных.

### Модель, построение и оптимизация:
- модель на основе градиентного бустинга: &nbsp; `XGBRegressor()`;
- подбор параметров: &nbsp; `early_stopping_rounds`, `GridSearchCV()`, `optuna`;
- валидация и оценка: &nbsp; `train_test_split()`, `cross_val_score()`.

