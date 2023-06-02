# Python - Obtendo o código fonte de uma página

~~~python
import requests

def retorna_response(url):
  response = requests.get(url)
  return response.text

response = retorna_response('https://www.inf.ufrgs.br/site')
print(response)
~~~
