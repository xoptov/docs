Правила программирования
========================

*Если есть вероятность того, что какая-нибудь неприятность может случиться, то она обязательно произойдёт. Э. Мерфи* 

Принцип [YAGNI](http://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
-------------
(You aren't gonna need it.)

Мы не делаем функционал, который не нужен. Не нужно создавать дополнительные классы, и прочее в надежде что это будет использовано.
В задаче решаем задачу, не трогаем другой функционал.

*Например: если нужно вывести статусы сделок в списке клиентов, нужно вывести статусы сделок. 
Вывод информации со сделками, платежами и прочим является избыточным.*

Принцип [SOLID](http://en.wikipedia.org/wiki/SOLID_%28object-oriented_design%29)
-------------
(Single responsibility, Open-closed, Liskov substitution, Interface segregation and Dependency inversion)

S - По этому принципу ваш код должен отвечать за один определенный функционал.
O - открыт к расширению, закрыт к изменению. (касается бандлов)
L - использование прототипирования. Код должен говорить объект какого интерфейса должен быть передан в класс, а не просто переменная.
I - разделение интерфейсов. Лучше использовать специфичные интерфейсы и в классе реализовывать несколько интерфейсов, вместо 1 большого.
D - включаем в зависимости только нужные сервисы с меньшим. [Dependency Injection](http://en.wikipedia.org/wiki/Dependency_injection)

Принцип [DRY](http://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
-------------
(don’t repeat yourself)

По этому принципу нужно недопускать дублирование кода, HTML, CSS, PHP, JS - неважно. Код или информация должна изменяться в 1 месте.

Принцип [KISS](http://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
-------------
(Keep it simple, stupid)

Смысл этого принципа - уменьшение сложности кода. Проще код - быстрее можно разобраться и сделать задачу.

Названия
-------------

Названия классов, методов, переменных должны [соответствовать стандартам](https://github.com/php-fig/fig-standards/tree/master/accepted).

Ниже пример правильного синтаксиса кода:

<pre><code>
<?php

namespace Vendor\Package\Feature[\Class]

use Vendor\Package\Feature\ClassOne;

class CamelCaseNaming
{
    const UPPER_CASE_CONSTANT = 1;
    const CONSTANTS_ABOVE_ALL = 2;

    public $publicProperty;

    protected $thenProtectedProperty;

    private $lastIsPrivateProperty;

    public function __construct(ClassOne $classOne)
    {
        $this->publicProperty = $classOne;
    }

    public function firstGoesPublicMethod()
    {
        foreach($this->publicProperty as $key => $value) {
            $value++;
        }
        
        if (isset($spaceBeforeReturn)) {
        
        }

        return $spaceBeforeReturn;
    }
}

</code></pre>
