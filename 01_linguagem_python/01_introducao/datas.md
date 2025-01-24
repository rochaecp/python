# Datas

## Criar

~~~python
from datetime import date, datetime

# date
minha_data = date.today()                      # 2025-01-24
minha_data = date.today().strftime('%d/%m/%Y') # 24/01/2025
minha_data = date.today().year      # 2025
minha_data = date.today().month     # 1
minha_data = date.today().weekday() # 4
minha_data = date.today().day       # 24
minha_data = date.today().hour      # 19
minha_data = date.today().minute    # 27
minha_data = date.today().second    # 10

# datetime
minha_data = datetime.now() # 2025-01-24 19:13:05.998820
minha_data = datetime.today() # 2025-01-24 19:13:05.998819
minha_data = datetime.now().strftime('%d/%m/%Y - %H:%M:%S') # 24/01/2025 - 19:22:20
minha_data = datetime(2023, 6, 27, 19, 27, 30).strftime('%d/%m/%Y - %H:%M:%S') # 27/06/2023 - 19:27:30
~~~

<!-- ****************************************************************************************** continuar revisão aqui -->

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