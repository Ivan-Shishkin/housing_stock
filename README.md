# Описание проекта

В вашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Ваша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. 
По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма. 

# Описание данных

1. `airports_nearest` — расстояние до ближайшего аэропорта в метрах (м)
2. `balcony` — число балконов
3. `ceiling_height` — высота потолков (м)
4. `cityCenters_nearest` — расстояние до центра города (м)
5. `days_exposition` — сколько дней было размещено объявление (от публикации до снятия)
6. `first_day_expositio` — дата публикации
7. `floor` — этаж
8. `floors_total` — всего этажей в доме
9. `is_apartment` — апартаменты (булев тип)
10. `kitchen_area` — площадь кухни в квадратных метрах (м²)
11. `last_price` — цена на момент снятия с публикации
12. `living_area` — жилая площадь в квадратных метрах(м²)
13. `locality_name` — название населённого пункта
14. `open_plan` — свободная планировка (булев тип)
15. `parks_around3000` — число парков в радиусе 3 км
16. `parks_nearest` — расстояние до ближайшего парка (м)
17. `ponds_around3000` — число водоёмов в радиусе 3 км
18. `ponds_nearest` — расстояние до ближайшего водоёма (м)
19. `rooms` — число комнат
20. `studio` — квартира-студия (булев тип)
21. `total_area` — площадь квартиры в квадратных метрах (м²)
22. `total_images` — число фотографий квартиры в объявлении

*Пояснение: апартаменты — это нежилые помещения, не относящиеся к жилому фонду, но имеющие необходимые условия для проживания.*

# План проекта

1. **Открыть файл с данными и изучить общую информацию**

   *Промежуточный вывод 1*


2. **Предобработка данных**
    - `airports_nearest`
    - `balcony`
    - `ceiling_height`
    - `cityCenters_nearest`
    - `days_exposition`
    - `first_day_expositio`
    - `floor`
    - `floors_total`
    - `is_apartment`
    - `kitchen_area`
    - `last_price`
    - `living_area`
    - `locality_name`
    - `open_plan`
    - `parks_around3000`
    - `parks_nearest`
    - `ponds_around3000`
    - `ponds_nearest`
    - `rooms`
    - `studio` 
    - `total_area`
    - `total_images`  
    
   *Промежуточный вывод 2*
   
    
3. **Посчитать и добавить в таблицу**

    - цену квадратного метра
    - день недели, месяц и год публикации объявления
    - этаж квартиры; варианты — первый, последний, другой
    - соотношение жилой и общей площади, а также отношение площади кухни к общей
    
   *Промежуточный вывод 3*
     
    
4. **Провести исследовательский анализ данных**

    - Изучить следующие параметры: площадь, цена, число комнат, высота потолков. Построить гистограммы для каждого параметра.
    - Изучить время продажи квартиры. Постройте гистограмму. Посчитать среднее и медиану. Описать, сколько обычно занимает продажа. Когда можно считать, что продажи прошли очень быстро, а когда необычно долго?
    - Уберать редкие и выбивающиеся значения. Описать, какие особенности обнаружили.
    - Какие факторы больше всего влияют на стоимость квартиры? Изучить, зависит ли цена от площади, числа комнат, удалённости от центра. Изучить зависимость цены от того, на каком этаже расположена квартира: первом, последнем или другом. Также изучить зависимость от даты размещения: дня недели, месяца и года.
    - Выбрать 10 населённых пунктов с наибольшим числом объявлений. Посчитать среднюю цену квадратного метра в этих населённых пунктах. Выделить среди них населённые пункты с самой высокой и низкой стоимостью жилья. 
    - Изучить предложения квартир: для каждой квартиры есть информация о расстоянии до центра. Выделить квартиры в Санкт-Петербурге ('locality_name'). Выяснить, какая область входит в центр. Построить график зависимости цены от удаленности от центра в км. Точку, в которой график значительно изменит свой характер принять за радиус центральной зоны.
    - Выделить сегмент квартир в центре. Проанализировать эту территорию и изучить следующие параметры: площадь, цена, число комнат, высота потолков. Также выделить факторы, которые влияют на стоимость квартиры (число комнат, этаж, удалённость от центра, дата размещения объявления).
    
   *Промежуточный вывод 4*
    
    
5. **Общий вывод**

