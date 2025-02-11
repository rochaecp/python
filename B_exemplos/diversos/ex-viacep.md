# Python - webservice viacep

~~~python
import requests

response = requests.get("http://viacep.com.br/ws/91786599/json/")

print(response.status_code)   # 200 == sucess, 400 == not found
print(response.text)          
data_cep = response.json()   
print(data_cep["logradouro"])
~~~
