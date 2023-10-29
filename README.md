Весь наш код находится в файле “NER for title and description of video HAKATON.ipynb”. Внутри ноутбука есть разделение на части:
  1) 1000 и 1 функция - объявление функций для выделение сущностей.
  2) Загрузка датасета - выгружает данным нам датасет и приводит его к нормальному формату.
  3) Приведение меток датасета к формату BIO - изначально данные о разметке хранятся в таком формате: 
     {'label': 'Дата', 'offset': 0, 'length': 15, 'segment': '14 октября 2023'}
	
     Мы приводим этот формат в этот:
	   O O O O B-Дата I-Дата I-Дата

  4) Pipeline: dataset to prediction - Создает удобный цикл обработки  от выгрузки датасета до получения предсказаний моделью
  5) Подсчет метрик - В этой части считаются f1 для каждого класса, а также среднее f1
  6) playground - В этой части ноутбука можно вводить кастомные данные и посмотреть какое предсказание выдаст модель
  7) Дополнительно - состоит из отладочных функций
  8) тестовый датасет - Обработка тестового датасета


В файле “NER dop.ipynb” прописаны некоторые дополнительные функции: как и что можно еще использовать для системы рекомендаций. Этот файл ники не влияет на “NER for title and description of video HAKATON.ipynb”. 
