# JavaTest
Ответы на вопросы теста 15.11.09

1. Какова разница между абстрактным классом и интерфейсом? 
Абстрактный класс – класс, который содержит абстрактные методы. Эти методы определены, но не
реализованы. Их реализация возможна в классах, которые являются наследниками
(extends) от исходного абстрактного.
Интерфейс – это аналог абстрактного класса. Он также определяет методы,
которые подлежит реализовать классам, применяющим (implements) данный
интерфейс. Отличие его от абстрактного класса состоит в том, что:
• Интерфейс не обладает ни одним реализованным методом, тогда как
абстрактный класс может иметь реализованные методы
• Произвольный класс может применять несколько интерфейсов, а
наследование разрешено только от одного класса-родителя.

2. Как «насильно» вызвать сборку мусора? 
Насильная сборка мусора вызывается методом finalize(), в случае если необходимо удалить неиспользуемый объект. В
методе можно определить набор действий, происходящих при этом. Использовать
данный метод не рекомендуется, поскольку сборка мусора производится
автоматически, а вызов метода не гарантирует его незамедлительное исполнение.

3. Когда требуется явное приведение классов? 
Явное приведение классов требуется в случае нисходящего преобразования: если необходимо изменить тип
переменной класса от класса-родителя (интерфейса) к классу-наследнику (классу,
применяющему интерфейс).

4. Чем конструкторы отличаются от других методов? 
Конструктор – это метод, который вызывается для создания экземпляра какого-либо нестатического класса.
Имеет то же имя, что и класс. При отсутствии в классе явно определенного
конструктора, вызывается конструктор по умолчанию. Конструкторы могут быть
перегружены. Если данный класс является наследником от класса-родителя,
первой операцией конструктора класса будет вызов конструктора класса-
родителя.

5. Можно ли вызывать конструкторы один из другого, если их в классе несколько?
Можно, если это перегруженные конструкторы (с разным набором входных
данных) 

6. JВ чем разница между JDK и JRE? 
DK – Java Development Kit – это среда разработки
приложений на Java. Содержит виртуальную машину, набор библиотек с исходным
кодом, компилятор, документацию
JRE – Java Runtime Enviroment – это программная среда для запуска Java-
приложений. Содержит виртуальную машину и набор стандартных библиотек.

7. Имеет ли значение в каком порядке перехватывать исключения FileNotFoundException и IOExceptipon?


8. Могут ли внутренние классы, описанные внутри метода, иметь доступ к локальным
переменным этого метода? 
Да, могут. Для этого при обращении используется спецификатор super
super.methodName();
super.Constructor();

9. В чем разница между очередью и стеком? 
Очередь - это последовательная структура данных, при которой элементы расположены друг за другом. При
односторонней очереди элементы располагаются по принципу "первый пришел -
первый ушел". В двусторонней очереди возможно движение элементов в оба
направления. Стек же реализует схему LIFO (Last In, First Out) – последний
пришел, первый вышел.

10. Что вам приходит в голову, когда вы слышите о новом поколении (young
generation) в Java? 
Данный термин принадлежит описанию Java virtual machine.В
young generation хранится большая часть созданных объектов. Если объекты
длительно сохраняются в памяти и сборщики мусора их не уничтожают, то они
переводятся в другие разделы - old generation

11. Есть два класса: A и B. Класс B должен информировать класс A когда случается некое важное событие. Какой design-pattern вы должны реализовать?

12. Какой модификатор доступа надо указать в классе, чтобы доступ к нему имели
только классы из того же пакета? 
Никакой, поскольку данный модификатор в Java
является модификатором по умолчанию(default).

13. Чем отличается статический внутренний класс от просто внутреннего класса?
Статические внутренние классы не имеют доступа к нестатическим полям и
методам внешнего класса. Доступ к нестатическим полям и методам может
осуществляться только через ссылку на экземпляр внешнего класса.

14. можно ли обратиться к не-статической переменной из статического метода?
Можно, если эта переменная уже проинициализирована в каком-либо классе

15. какие типы данных есть в Java?
String - строка
целочисленные типы: byte, short, int, long
логический тип: boolean
дробные типы: float, double
символьный тип: char

16. Чем отличаются переопределение (Override) и перегрузка (Overload)
Переопределение метода – это переписывание метода, унаследованного от
класса-родителя. Перегрузка метода – это создание методов, обладающих одним
общим названием, но разным набором переменных. Фактически при этом
создаются разные методы, которые различает компилятор.

17. Что такое итератор? 
Итератор – это метод, с помощью которого производится
просмотр элементов списка

18. Перечислите основные категории исключительных ситуаций 
Контролируемые исключения (checked), неконтролируемые исключения (unchecked), к которым
относятся ошибки (Errors), и исключения времени выполнения
(RuntimeExceptions).

19. Какая разница между throw и throws?
 throw это - операция, которая производит искусственную генерацию
исключительной ситуации, в то время как throws - это идентификатор метода,
означающий, что метод может выбрасывать исключительную ситуацию.
