# timer-js-

JS-код для таймера (обратный отсчет времени от сейчас до определенной даты)

1. Необходимо определить в переменную конечную дату отсчета таймера.

2. Создаем функцию getTimeRemaining(endtime), которая будет рассчитывать время в промежутке между сейчас и конечной датой. В этой функции создаем переменные, в которые присваем общее количество оставщегося времени в миллисекундах, а также отдельно секунды, минуты, часы и при необходимости дни.
После возваращаем значения полученных переменных.

3. Создаем функцию setClock(id, endtime), которая превратит статическую верстку в динамическую (то есть запустит сам таймер). В этой функции необходимо получить сам таймер, дни, часы, минтуы и секунды, которые находятся в таймере. Также необходимо создать переменную, в которую поместить значение интервала обновления для функции updateClock() (то есть как часто таймер будет обновляться: 1 секунда).

  3.1. Создаем функцию updateClock(), которая будет обновлять таймер каждую секунду. Внутри также создаем функцию addZero(num), которая будет добавлять ноль перед числом, если число меньше девяти (то есть вместо 9:18:3 будет 09:18:03). После присваиваем полученным в функции setClock(id, endtime) переменным значения из функции getTimeRemaining(endtime) (не забывая при этом про функцию добавления нулей).

  3.2. И наконец выставляем условие, при котором таймер будет останавливать свою работу и выставлять значения времени в ноль, если общее значение оставшегося времени до dedline равно меньше нуля.

4. Запускаем работу функции setClock(id, endtime), где в качестве аргументов указываем id таймера и переменную, определенную в первом пункте.
