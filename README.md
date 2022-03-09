# JavaTask1
Java HW 2.03.2022 AT-03

## Задание 1

![Скрин 1](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2011.54.52.09.png)

Создал репозиторий на гите.

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2011.59.22.41.png)

Написал код и запушил в этот репозиторий.

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2012.15.24.08.png)

Добавил новую фичу и закинул её в новую ветвь (feature1).

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2012.20.53.38.png)

С помощью команды git merge слил ветку feature1 в main. 

## Задание 2 

### Maven

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.22.14.14.png)

Собираю jar-файл через maven.

```java
import org.jfree.chart.ChartFactory;
import org.jfree.chart.ChartUtilities;
import org.jfree.chart.JFreeChart;
import org.jfree.data.general.DefaultPieDataset;

import java.io.File;

public class Main {
    public static void main(String[] args) {
        DefaultPieDataset pieDataset = new DefaultPieDataset();
        pieDataset.setValue("a", 30);
        pieDataset.setValue("b", 70);

        JFreeChart chart = ChartFactory.createPieChart(
                "title",
                pieDataset,
                true,
                false,
                false
        );

        try{
            ChartUtilities.saveChartAsJPEG(new File("C:\\Users\\Miarel\\Desktop\\123.jpeg"),
                    chart,
                    1920,
                    1080);
            System.out.println("project built");
        }
        catch (Exception e)
        {
            System.out.println(e);
        }
    }
}

```

Указал в xml библиотеку jfree для построения графиков и т.п. То есть в результате выполнения программы мы должны получить круговую диаграмму с 2-мя секторами и сообщение "project built" если всё прошло успешно

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.28.24.91.png)

Запускаю jar-файл из командной строки.

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.28.32.35.png)

Результат.

### Gradle

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.28.58.07.png)

Подобным образом создаю jar-файл в gradle.

```java
import org.jfree.chart.ChartFactory;
import org.jfree.chart.ChartUtilities;
import org.jfree.chart.JFreeChart;
import org.jfree.data.general.DefaultPieDataset;

import java.io.File;

public class Main {
    public static void main(String[] args) {
        DefaultPieDataset pieDataset = new DefaultPieDataset();
        pieDataset.setValue("a", 30);
        pieDataset.setValue("b", 70);
        pieDataset.setValue("c", 20);
        pieDataset.setValue("d", 55);
        pieDataset.setValue("e", 16);

        JFreeChart chart = ChartFactory.createPieChart(
                "title",
                pieDataset,
                true,
                false,
                false
        );

        try{
            ChartUtilities.saveChartAsJPEG(new File("C:\\Users\\Miarel\\Desktop\\123.jpeg"),
                    chart,
                    1920,
                    1080);
            System.out.println("project built");
        }
        catch (Exception e)
        {
            System.out.println(e);
        }
    }
}

```

Добавил секторов на диаграмму.
![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.29.42.59.png)

Запуск в IDE.

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2019.29.50.36.png)

Результат.
## Задание 3

![Скрин 2](https://github.com/Miarel/JavaTask1/blob/main/Screenshots/Desktop%20Screenshot%202022.03.09%20-%2012.28.12.02.png)

Версия Java.
