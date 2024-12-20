### Выбросы в данных. Как работать с выбросами

1. `Что такое выбросы в данных`

    Выбросы — это значения, которые значительно отличаются от других данных и не вписываются в общую картину. Они могут 
возникать из-за ошибок при вводе данных, различных технических сбоев или из-за того, что они представляют необычные, но 
возможные события. Выбросы могут искажать результаты анализа и ухудшать качество моделей.

2. `Как работать с выбросами`

    Существует несколько подходов к работе с выбросами, и выбор метода зависит от цели анализа и характера данных.

 - `Удаление выбросов`

    Если выбросы возникли из-за ошибок в данных, их можно удалить, чтобы они не искажали результаты анализа. Этот метод подходит, когда выбросы составляют небольшую часть данных и явно ненормальны.

    Пример: Если в данных о возрасте указано значение 150, его можно удалить как ошибку, так как это значение биологически невозможно.

 - `Замена выбросов`

    Выбросы можно заменить на более типичные значения, например, среднее, медиану или значения соседних данных. Это 
может быть полезно, когда удаление выбросов не желательно.

    Пример: Если в данных о доходах есть несколько значений, которые намного выше среднего и они кажутся ошибочными, их 
можно заменить на медианный доход.

 - `Трансформация данных`

    Иногда выбросы можно "сгладить" с помощью трансформации данных, например, логарифмической или корневой, чтобы 
уменьшить влияние выбросов на анализ. Этот метод полезен, когда распределение данных асимметрично.

    Пример: Если данные о доходах сильно искажены из-за больших значений, можно применить логарифмическую трансформацию,
чтобы сделать распределение более равномерным.

 - `Использование робастных методов`

    В некоторых моделях выбросы могут не оказывать значительного влияния. Например, медиана и интерквартильный размах 
(IQR) являются робастными метриками, менее чувствительными к выбросам, чем среднее или дисперсия.

    Пример: При анализе данных с выбросами можно использовать медиану вместо среднего, чтобы избежать искажения значений.

 - `Создание отдельной категории`

    Если выбросы имеют смысл для анализа, их можно сохранить в отдельной категории. Это позволяет модели учитывать 
необычные значения, не искажая общую картину данных.

    Пример: В продажах могут быть аномально высокие значения в праздничные дни. Вместо того чтобы удалять их, можно 
создать отдельную категорию "праздничные дни" и анализировать их отдельно.

3. Примеры и выбор метода

 - Пример 1: В финансовых данных некоторые транзакции сильно отличаются от остальных. Если такие выбросы могут быть 
ошибочными, их стоит удалить. Если же они отражают редкие, но реальные события, можно создать отдельную категорию.

 - Пример 2: В данных о росте и весе населения выбросы могут быть вызваны ошибками ввода. Если указаны нереалистичные 
значения (например, рост 2.5 метра), такие значения можно удалить или заменить на медианные.

 - Пример 3: В данных о продажах несколько магазинов могут показывать аномально высокие или низкие показатели. Вместо 
удаления выбросов можно использовать робастные методы анализа, такие как медиана или интерквартильный размах, чтобы 
данные остались в выборке, но не сильно влияли на результат.

Итог: Работа с выбросами необходима для улучшения качества анализа и повышения устойчивости моделей. Выбор метода 
зависит от источника выбросов, структуры данных и цели анализа.
