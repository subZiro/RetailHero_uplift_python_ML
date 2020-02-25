# RetailHero_uplift_python_ML
Решение ML соревнования по Uplift Modelling ['Каким клиентам нужно отправить SMS?'](https://retailhero.ai/c/uplift_modeling/overview)

## Best Public Leadboard: 0,0932

## Описание подхода

Всего признаков 200:
  * Корректировка возростного вброса <14 и >90 
  * Возрастные категории кратно 10
  * Кол-во и сумма покупок
  * Суммы покупок, отмеченных флагами "алкоголь", "own trademark"

Моделирование происходит функцией взятой из базовой модели

Для построения моделей используется GradientBoostingClassifier. Так же рассматривались xgboost,lightgbm и RandomForestClassifier. Корректировка возрастов строится на модели lightgbm.

## Описание файлов:

	info.docx - краткая информация о соревновании

	uplift_model_v4.5.ipynb - Uplift модель, обработка данных и предсказание модели в одном файле. 
	Лучший результат на GradientBoostingClassifier() - Public = 0,0782
	
	submission_v4_05_02_22.csv - результат предсказания - Public = 0,0782, Private = 0,083865

	Public = 0,0930, Private = 0,091635
	
	uplift_model_v5.5.ipynb - Uplift модель, обработка данных и предсказание модели в одном файле. 
	Лучший результат на GradientBoostingClassifier() - 0,0930 






## Ссылки

Cайт соревнования  [X5 Retail Hero](retailhero.ai/c/uplift_modeling/overview)

Код создания фич взят из [nersirion-RetailHero.ai-uplift](https://github.com/nersirion/nersirion-RetailHero.ai-uplift) by nersirion
