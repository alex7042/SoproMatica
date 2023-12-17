# SoproMatica
Приложение SoproMatica предназначено для инженеров, работающих в сфере проектирования (в первую очередь металлоконструкций), а также студентов, обучающихся на соответствующих направлениях.
Начальный экран содержит навигацию по трем основным модулям приложения:
- Расчет балок - в данном модуле составляется расчетная схема балки, производится расчет реакций опор и/или заделок и построение эпюр изгибающих моментов и перерезывающих сил;
- Справочник (в разработке) - данный модуль содержит основные теоретические положения по расчетам прочности и устойчивости металлоконструкций;
- Конвертер (в разработке) - данный модуль предназначен для конверсии единиц измерения физических величин

Анимация логотипа на начальном экране реализована с помощью AnimationUtils. Логотип создан в AutoCad и доработан в Inkscape. Макет интерфейса разработан в Adobe XD.

![](https://github.com/alex7042/SoproMatica/blob/main/App%20preview%20gifs/01_startMenu.gif)
  
В модуле "Расчет балок" на первом фрагменте задаются параметры балки, такие как: длина, количество опор и тип закрепления концов балки. Навигация по модулю реализована с помощью BottomNavigationBar и ViewPager2 с кастомными иконками.
Для ввода даннных используется AlertDialog.

![](https://github.com/alex7042/SoproMatica/blob/main/App%20preview%20gifs/02_addBeamParameters.gif)

На втором фрагменте задаются нагрузки на балку, такие как: сосредоточенная сила, момент и равномерно/неравномерно распределенная нагрузка (трапециевидная, треугольная). Для отображения списков используется ConcatAdapter с вложенными RecyclerView.

![](https://github.com/alex7042/SoproMatica/blob/main/App%20preview%20gifs/03_addBeamLoads.gif)

При необходимости, веденные данные можно удалять и редактировать.

![](https://github.com/alex7042/SoproMatica/blob/main/App%20preview%20gifs/04_recreateBeamLoads.gif)

Под BottomSheet, отображаются эпюры перерезывающих сил и изгибающих моментов.

![](https://github.com/alex7042/SoproMatica/blob/main/App%20preview%20gifs/05_resultGraphs.gif)

На данном этапе в приложении реализована возможность расчета реакций опор и построения эпюр для статически определимых балок аналитическим методом.
