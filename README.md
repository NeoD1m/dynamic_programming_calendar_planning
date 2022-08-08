# Калькулятор задачи о календарном планировании

Если не определено минимальное кол-во рабочих, устанавливайте значение равное минимальным требованиям.

## Условие задачи</summary>
  
  На период Т дней известен объем погрузо-разгрузочных работ,
выражаемый в ежедневной потребности в рабочих d(t), t=1,2,…,T. Рабочих
можно ежедневно нанимать и увольнять. При нехватке рабочих прибегают к
сверхурочным работам, и затраты возрастают на C1 за каждого
недостающего рабочего.
Расходы на содержание одного незанятого рабочего составляют C2,
найм одного рабочего C3 ,
увольнение требует расходов C4.
Составить оптимальный план регулирования численности рабочих за Т
дней, если исходное количество рабочих равно R
  


## Как читать результат?

Калькулятор строит T таблиц для каждого дня. В первом столбце указано кол-во рабочих в предыдущем отчётном периоде, в заголовках следующих столбцов указано кол-во рабочих для следующего отчётного периода. Крайний правый столбец содержит минимальную стоимость дня для каждого варианта кол-ва рабочих в предыдущий день. В содержании таблицы указана стоимость дня для каждого возможного варианта.

### Пример чтения таблицы
Алгоритм чтения таков: смотрим в левый столбец и выбираем из него сколько у нас уже есть рабочих, из заголовков следующих столбцов выбираем желаемое кол-во и на пересечении видим стоимость этого перехода. Зелёным выделена самая эффективная стратегия. Оранжевым выделена оптимальная стратегия для каждого варианта начального кол-ва рабочих.

Рассмотрим пример чтения табоицы для одного из дней тестового варианта.  День 7, требуется 17 рабочих. Наиболее эффективной стратегией является уже иметь к этому дню 17 рабочих и не проводить никаких наймов и увольнений. Это логично и будет стоить 90 у.е. Если бы у нас было 10 рабочих, то эффективнее всего было бы нанять 7 рабочих и это стоило бы 216 у.е.
![](https://github.com/L3odr0id/dynamic_programming_calendar_planning/blob/master/explanation3.jpg)

Этот пример кажется очевидным, но рассмотрим второй день для этого же тестового варианта. Требуется всего 6 рабочих, но наиболее эффективная стратегия - это стартовать с 14 рабочих. Впрочем, если у вас уже есть 6 рабочих, выгоднее никого не нанимать. А если у вас в команде менее 6 рабочих, выгоднее всего нанять недостающих.
![](https://github.com/L3odr0id/dynamic_programming_calendar_planning/blob/master/explanation2.png)

![visitors](https://visitor-badge.glitch.me/badge?page_id=l3odr0id.dynamic_programming_calendar_planning) <!-- set 07.08.2022 -->
