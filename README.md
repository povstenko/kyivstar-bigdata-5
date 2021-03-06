# Kyivstar Big Data School 5.0
Kyivstar Big Data School 5.0 task of 2'nd stage of the selection

[Big Data School Page](https://bigdata.kyivstar.ua/school/)

## Перевіряємо, що було завантажено і навіщо.

Архів містить 4 файли:
* tabular_data.csv
* hashed_feature.csv
* train.csv
* test.csv

### Для чого вони?

Ці файли допоможуть вирішити аналітичну задачу. Необхідно побудувати модель, що виявлятиме сегмент водіїв серед абонентів ПрАТ «Київстар».

Це задача бінарної класифікації:  
**«1»** – абонент являється водієм (відноситься до сегменту водіїв), 
**«0»** – абонент не є водієм (не відноситься до сегменту водіїв).

Файли **tabular_data.csv** і **hashed_feature.csv**  ̶  тут описові характеристики щодо 4084 абонентів («ID» – це ідентифікатор абонента).
Файл **train.csv**  ̶  це дані щодо цільової мітки (чи належить абонент до сегменту водіїв).
Файл **test.csv**  ̶  це список абонентів, для яких необхідно зробити прогноз, за яким ми й будемо оцінювати якість ваших моделей.

### А тепер детальніше:

* Файл **tabular_data.csv** містить числові дані щодо активності абонента за 12 періодів.  
	* period – номер періоду (періоди послідовні, 1 – найновіший);
	* id – ідентифікатор абонента;
	* feature_0 – feature_49 – дані щодо активності абонента у відповідний період.
* Файл **hashed_feature.csv** – тут набір захешованих значень однієї категоріальної змінної для абонента.
	* id – ідентифікfeature_50 – хеш від значення категоріальної змінної.атор абонента;
	* feature_50 – хеш від значення категоріальної змінної.
* Файл **train.csv** – тут дані з цільовою міткою.
	* id – ідентифікатор абонента;
	* target – значення цільової мітки (1 – належить до сегменту водіїв, 0 – не належить до сегменту водіїв).
* Файл **test.csv** – список абонентів, для яких потрібно зробити передбачення за допомогою ваших моделей.
	* id – ідентифікатор абонента;
	* score – ймовірність того, що абонент належить до сегменту водіїв (класу «1»). Цю ймовірність визначає ваша модель

>До речі, моделі ми будемо оцінювати за такою метрикою – [ROC-AUC](https://uk.wikipedia.org/wiki/ROC-%D0%BA%D1%80%D0%B8%D0%B2%D0%B0).

## У чому ж завдання?

Потрібно побудувати модель на абонентах, цільова мітка по яким міститься у файлі **train.csv**.

Для цього вам необхідно використати дані з файлів **tabular_data.csv** та **hashed_feature.csv**. Після цього, використовуючи вашу модель, потрібно для абонентів з файлу **test.csv** заповнити колонку **score** – ймовірність того, що абонент відноситься до сегменту водіїв. Зверніть увагу, що необхідно спрогнозувати факт відношення до сегменту водіїв, без прив'язки до періоду.

## Оформлення рішення – зберігаємо результати

Зберігаємо передбачене значення **score** для тестової вибірки у файл **MoyePrizvyshcheMoyeImya_test.csv**, де **MoyePrizvyshcheMoyeImya** = ваше прізвище і ваше ім'я.

Ми хочемо, щоб ви назвали свій файл унікально, про всяк випадок :)

## Оформлення рішення – зберігаємо код

Зберігаємо код програми в файл **MoyePrizvyshcheMoyeImyaPROGRAM.?** Залежно від мови програмування, у файлі буде відповідне розширення: **.R**, або **.py** або **.txt** або ще яке-небудь.

Наприклад:
* **MoyePrizvyshcheMoyeImyaPROGRAM.R**,
* **MoyePrizvyshcheMoyeImyaPROGRAM.py**,
* **MoyePrizvyshcheMoyeImyaPROGRAM.txt** і т.д.

## Надсилаємо рішення

Готове рішення (файли з результатом та кодом) завантажуємо одним архівом у форматах **.zip** або **.rar** у спеціальну форму [на сайті](https://bigdataschool.esclick.me/D3p8ZMv0yMuu).

## Чекаємо на результати

Тепер можна відпочивати і чекати від нас листа :)

### Що буде в листі?
За результатами перевірки завдання вам може бути запропоновано пройти наступний етап тестування.

Лише після проведення 2-х етапів тестування будуть розіслані остаточні відповіді – про зарахування до школи чи відмову.

* Орієнтовна дата розсилки листів для співбесіди – **13 жовтня**.
* Дати проведення співбесід – **14-16 жовтня**.

**Тож усі відповіді ви отримаєте до 23 жовтня.**

## FAQ:

### Які інструменти я можу використовувати для вирішення тестового завдання? 
Для виконання тестового завдання ви можете використовувати будь-які інструменти та алгоритми. У свою чергу, ми рекомендуємо використовувати імплементовані у **Python** чи **R**.

### Деякі значення є пропущеними. Що з ними робити?
Нас цікавить, як ви будете вирішувати проблему пропуску даних. Тому це повністю ваш вибір.

### Як будуть порівнюватись результати моделей?
Метрика, за якою ми будемо оцінювати якість ваших моделей, – **ROC-AUC**.

Бажаємо гарного і творчого настрою та з нетерпінням чекаємо на ваші результати!

Залишаймось на зв’язку,  
Big Data School від Київстар.
