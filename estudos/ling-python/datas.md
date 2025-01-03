# Datas

## Criar

~~~python
print(date.today())
print(date.today().strftime('%d/%m/%Y'))
print()
print(datetime.today())
print(datetime.now())
print(datetime.now().strftime('%d/%m/%Y - %H:%M:%S'))
print()
data_1 = datetime(2023, 6, 27, 19, 27, 30)
print(data_1.strftime('%d/%m/%Y - %H:%M:%S'))
print()
~~~

~~~python
from datetime import date

current_date = date.today()
current_date = date.today().strftime('%d/%m/%Y') 
~~~

~~~python
from datetime import datetime

current_date = datetime.now()
current_date = datetime.now().strftime('%d/%m/%Y - %H:%M:%S')

my_year = current_date.year
my_month = current_date.month
my_weekday = current_date.weekday()
my_day = current_date.day
my_hour = current_date.hour
my_minute = current_date.minute
my_second = current_date.second
~~~

~~~python
my_personal_date = datetime(2021, 3, 24, 15, 40, 20)
~~~

~~~python
my_tuple = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday")
my_day = my_tuple[current_date.weekday()]
~~~

~~~python
date_string = "01/01/2019"
date_formated = datetime.strptime(date_string, "%d/%m/%Y")
~~~

~~~python
from datetime import time

my_time = time(hour=17, minute=11, second=30)
my_time = time(hour=17, minute=11, second=30).strftime('%H:%M:%S')
~~~


~~~python
from datetime import datetime, timedelta
my_date = datetime(2021, 3, 30)
new_date = my_date - timedelta(days=365, hours=2, minutes=15)
~~~

## Extrair

~~~python
hoje = datetime.today()
print(hoje.year)
print(hoje.month)
print(hoje.weekday())
print(hoje.day)
print()
print(hoje.hour)
print(hoje.minute)
print(hoje.second)
print()
~~~

## Converter

~~~python
date_string = "01/01/2019"
date_formated = datetime.strptime(date_string, "%d/%m/%Y")
print(date_formated)
print()
~~~

## Exemplo

~~~python
dias_sem_tupl = ("Seg", "Ter", "Qua", "Qui", "Sex", "Sab", "Dom")
print(dias_sem_tupl[hoje.weekday()])
~~~

## Time

~~~python
my_time = time(hour=17, minute=11, second=30)
my_time = time(hour=17, minute=11, second=30).strftime('%H:%M:%S')
~~~

## TimeDelta

~~~python
my_date = datetime(2021, 3, 30)
new_date = my_date - timedelta(days=365, hours=2, minutes=15)
~~~