

Soroka v2 Build Guide [RU]

### Необходимые инструменты и расходники:

- Паяльник с регулировкой температуры и тонкое конусное жало  
    Фото для примера:  
    

![](https://telegra.ph/file/67c95aea2ec2952f8d3aa.png)

Пример подходящего жала для установки инсертов

- Два тонких металлических пинцета, один из них можно заменить любой перемычкой типа скрепки
- Флюс для пайки и припой
- Медная оплетка для удаления припоя (в случае проблем с пайкой, опционально)
- Оловоотсос (опционально)
- Отвертка или шестигранник
- Суперклей
- Зубочистка или спичка
- Изопропиловый спирт или Flux-OFF
- Салфетки или тряпка для очистки излишков флюса

### Необходимые детали:

- Soroka v2 PCB, 1 шт
- Soroka v2 Plate, 1  шт
- Soroka v2 Case, 1  шт
- Soroka Spacer, 1  шт
- Диоды 1N4148W, SOD-123, 51  шт
- RP-2040 Zero, 1  шт
- Вплавляемые инсерты M2, 13  шт
- M2 винты, 4 мм, 13  шт    
- Овальные ножки 22x4x1.5mm, 4 шт
- Силиконовые шайбы 5 x 2 x 1, 9  шт
- Неодимовые магниты 3мм x 1мм, 8  шт
- Panasonic EVQWGD001 или 12.5 mm EC11 энкодер (Опционально), 1  шт

### Сборка PCB

**1. Проверить работоспособность контроллера.**

Для этого подключите контроллер к компьютеру с помощью USB кабеля, светодиод на нем начнет мигать.   
Затем необходимо зажать кнопку BOOT и в это же время кликнуть RESET. Компьютер должен обнаружить новое устройство и открыть папку накопителя. Можно сразу же закинуть файл прошивки в формате .uf2, просто перетащив файл в папку. После копирования файла, накопитель должен автоматически перезагрузится и выйти из режима прошивки. 

**2. Установить диоды.**

Необходимо смазать посадочные площадки диодов кисточкой с флюсом. Не стоит мазать все сразу, лучше идти по рядам. Нанести флюс на один ряд, припаять диоды, а затем повторить еще 3 раза.   
Диоды имеют полярность, поэтому важно располагать их нужно стороной.  
На диоде есть метка катода (светлая полоска на корпусе, со стороны одного из выводов), ее нужно расположить с замкнутой стороны белого прямоугольника на плате. Пример на фото: 

![](https://telegra.ph/file/cb34dd532b3d4c7d1779a.png)

**3. Установить контроллер.**

Контроллер необходимо расположить на той же стороне, что и диоды. Кнопки контроллера должны оказаться внутри выреза на плате и смотреть на лицевую (верхнюю) поверхность платы.

![](https://telegra.ph/file/2915a50b71b93e6455f77.png)

Для ровной и простой установки, можно использовать комплектные пины.   
Перед размещением контроллера, необходимо нанести флюс на площадки на плате и контроллере.

**ВАЖНОЕ ЗАМЕЧАНИЕ! Гребенки используются ТОЛЬКО для выравнивания, их НЕ НУЖНО припаивать.** 

Я устанавливаю комплектную гребенку снизу и с еще одной стороны и припаиваю пады на оставшейся. После этого, вынимаю гребенки и припаиваю остальные площадки контроллера. 

![](https://telegra.ph/file/da451aaff68b6bac8cfc1.png)

  

**4. Установить энкодер и припаять энкодер.**

В случае энкодера Panasonic, необходимо "зацепить" его за плату, а затем припаять все пины. 

![](https://telegra.ph/file/b771e24d885c8826160ce.png)

"Крюк", который необходимо зацепить за плату

  

5. Отмыть все следы пайки и остатки флюса с платы.

Обильно нанести спирт или очиститель и удалить все сухой тряпкой или салфеткой. В случае сильных загрязнений, можно оттереть сильные загрязнения зубной щеткой. 

**6. Проверить PCB после пайки.**

После высыхания платы, подключить USB-кабель. Если контроллер еще не прошит, см шаг 1.  
Последовательность проверки следующая:

- Запустить VIAL
- Перейти на вкладку Layout и установить все желаемые опции

![](https://telegra.ph/file/35c18577f3ca3a647ed96.png)

- Перейти на вкладку Matrix tester и кликнуть на кнопку Unlock

![](https://telegra.ph/file/015ea209bf08cbb2d3be2.png)

- При помощи двух пинцетов замкнуть пины первых двух свитчей в первом ряду и дождаться пока прогресс-бар разблокировки заполнится. 
- С помощью пинцета поочередно замыкать контактные площадки всех свитчей. Это позволит убедится, что пайка выполнена без ошибок.
- В случае, если не работают отдельные кнопки - необходимо проверить пайку соответствующих диодов, если не работает целый ряд или колонка - необходимо проверить пайку площадок контроллера. 

**7. Установить свитчи в плейт (опционально) и запаять свитчи с нужным лейаутом**.

Аккуратно удалить излишки флюса, если они есть. 

**8. Поздравляю, вы восхитительны!**  
 

### Сборка остальной клавиатуры

**0. Установить силиконовые ножки на дно кейса**

![](https://telegra.ph/file/56d6670780c6b335f92a5.png)

**1. Заплавить инсерты в посадочные места внутри корпуса**.

Для этого установите инсерт в посадочное отверстие корпуса, и нагретым паяльником, медленно опускайте его в вниз.

_ВАЖНО! Паяльник нужно держать перпендикулярно плоскости внутреннего дна. Не нужно прикладывать лишних усилий. Если инсерт тяжело заходит, немного увеличьте температуру или подождите пока все детали достаточно нагреются._ 

**2. Заплавить инсерты в проставку под панель.**

Инсерты расположены ближе к краям, отверстия под них более глубокие. Вот правильная сторона: 

![](https://telegra.ph/file/6cb2c28ec447410a2eb9b.png)

Места для установки инсертов

**3. Приклеить магниты в проставку.**

Рекомендую делать все поочередно, чтобы не запутаться с полярностью магнитов, иначе достать их будет невозможно, деталь будет испорчена.

  

![](https://telegra.ph/file/6798e671eddfcbcc69285.png)

Места для установки магнитов

  

Последовательность следующая:

- Выдавить каплю суперклея на листок бумаги или плотного картона
- С помощью зубочистки нанести немного клея в отверстие для магнита
- Установить магнит и удалить излишки клея

Повторить эту операцию для всех магнитов проставки. 

**4. Приклеить магниты для крышки.**

Очень важно приклеить нужно стороной. Последовательность действий: 

- Разместить магниты на уже приклеенных магнитах проставки. Это позволит узнать полярность и какой стороной нужно будет приклеивать.
- Чтобы исключить ошибки, можно поставить точки маркером на видимой поверхности магнита. Это будет та сторона, которая будет размещена внутри крышки. 
- Поочередно приклеивать магниты, как это было сделано для проставки. Точкой от маркера ВНУТРИ крышки.

**5. Прикрутить проставку к PCB винтами.** 

![](https://telegra.ph/file/22f273c7771307c592620.png)

Расположение винтов для проставки

**6. Установить силиконовые шайбы внутри посадочных мест корпуса**

![](https://telegra.ph/file/2b3a4265e1f0d8d9f1eb8.png)

Места установки силиконовых шайб

**7. Установить готовую PCB внутри корпуса, прикрутив винтами.** 

**8. Установить крышкечку на магнитах и кейкапы**

### Готово! 
