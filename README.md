# Отчет о тестировании KeyValidator 

## Краткое описание

  14.02.2020 было протестировано приложение KeyValidator (далее - KV), проверяющее лицензионные ключи. На тестирование предоставлены установочная [документация](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md) для среды [OpenJDK 11](https://adoptopenjdk.net/), само [приложение](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/artifacts/KeyValidator.class) KV и [руководство](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md) по его использованию. 

  На тестирование затрачен 1 час.

  В результате тестирования выявлены следующие дефекты:
* [баг-репорт 1](https://github.com/sergsemenov/Java1.1-homework-1/issues/1)
* [баг-репорт 2](https://github.com/sergsemenov/Java1.1-homework-1/issues/2)

## Процесс тестирования

### Что тестировалось
1. соответствие фактической установки OpenJDK 11 (LTS) и описанной в установочной документации;
1. совместимость KV с Java 11;
1. соответствие фактической работы KV и описанной в руководстве по использованию.

### Артефакты тестирования
* тест-план, описанный в [легенде](https://github.com/netology-code/javaqa-homeworks/tree/master/intro#%D0%BB%D0%B5%D0%B3%D0%B5%D0%BD%D0%B4%D0%B0);
* тест-сьют, состоящий из двух тест-кейсов: 
    * проверка валидных ключей (позитивный сценарий);
    * проверка невалидных ключей (негативный сценарий);
* баг-репорты;
* данный отчет о тестировании.

### Тестовые данные
  Для тестирования использовались [данные](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md#%D0%BA%D0%BB%D1%8E%D1%87%D0%B8-%D0%B4%D0%BB%D1%8F-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B8), указанные в [руководстве](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md). Ожидаемый результат для любого ключа из набора валидных ключей - сообщение "OK", для любого ключа из набора невалидных ключей - "FAIL". Любое поведение, отличное от указанного, должно рассматриваться как дефект и сопровождаться баг-репортом.

### Тестовое окружение
* Windows 8.1 Версия 6.3 (сборка 9600)
* Java openjdk version "11.0.6" 2020-01-14
* OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.6+10)
* OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.6+10, mixed mode)
* git version 2.25.0.windows.1

### Как производилось тестирование
Взаимодействие с KV осуществлялось посредством командной строки. 

<details>
  <summary> Два способа вызова окна команд</summary>

  * кликнуть правой кнопкой мыши на каталоге, где расположен файл KeyValidator.class, в контектном меню выбрать "git bash here";
  * с нажатой клавишей Shift кликнуть на названии каталога, где расположен файл KeyValidator.class, и выбрать "Открыть окно команд".
</details>

## Итоги тестирования
  Приложение KV на тестовых данных проверило успешно 7 из 10 ключей, при этом на проверке валидных ключей программа допустила 2 ошибки, на проверке невалидных 1 ошибку. Необходимо доработать код приложения.
