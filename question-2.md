### Производная. Производная сложной функции. Градиент. Градиенты простейших функций: MSE, Binary Cross-Entropy
<br/>

1. `Производная функции`

Производная — это инструмент, который показывает, как быстро изменяется значение функции в зависимости от изменения её 
переменной. Представьте, что у вас есть кривая, и производная в точке на этой кривой показывает угол наклона касательной
в этой точке. Чем больше значение производной, тем сильнее наклон. 

2. `Производная сложной функции (правило цепочки)`

Когда функция составлена из нескольких функций, например, 𝑓(𝑔(𝑥)), мы используем правило цепочки. Оно позволяет найти 
производную такой сложной функции по частям: сначала находим, как меняется внешняя функция 𝑓, а затем умножаем на то, 
как изменяется внутренняя функция 𝑔. Например, если мы хотим узнать скорость изменения температуры (внешняя функция), 
которая зависит от высоты над уровнем моря (внутренняя функция) и высоты, которую мы меняем по времени, мы используем 
правило цепочки.

3. `Градиент`

Градиент — это вектор, который показывает, в каком направлении функция увеличивается быстрее всего, и насколько быстро 
она увеличивается. Если представить, что функция — это рельеф с возвышенностями и впадинами, то градиент будет указывать
направление вверх по самому крутому склону. В задачах оптимизации он помогает найти, в какую сторону нужно сдвинуться, 
чтобы минимизировать (или максимизировать) значение функции.

4. `Градиенты простейших функций в машинном обучении`

 - `Среднеквадратическая ошибка (MSE)`

MSE используется для оценки, насколько точны предсказания модели в задачах регрессии. Она вычисляется как среднее 
квадратов разниц между истинными значениями и предсказанными. Если ошибка велика, градиент укажет направление и "сила" 
изменения модели, чтобы уменьшить ошибку.

 - `Бинарная кросс-энтропия (Binary Cross-Entropy)`

Используется для оценки качества предсказаний в задачах бинарной классификации (например, "да" или "нет"). Она измеряет,
насколько вероятности предсказания отличаются от реальных значений. Градиент показывает, в каком направлении менять 
параметры модели, чтобы предсказания были ближе к реальным меткам.