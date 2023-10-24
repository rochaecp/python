# Arquivos

## Escrevendo e atualizando arquivos de texto

~~~python
def write_file(name_file, txt):
    my_file = open(name_file, "w")
    my_file.write(txt)
    my_file.close()

def change_file(name_file, txt):
    my_file = open(name_file, "a")
    my_file.write(txt)
    my_file.close()

if __name__ == "__main__":
    change_file("my txt\n")
~~~

## Lendo arquivos de texto

~~~python
def le_my_file(name_file):
    my_file = open(name_file, "r")
    txt = my_file.read()
    linhas = txt.split("\n")
    print(linhas[0])
    print(linhas[-1])

if __name__ == "__main__":
    le_my_file("notes.txt")
~~~

## Copiando um arquivo

~~~python
import shutil    # biblioteca
def copy_my_file(name_file):
    shutil.copy(name_file, "./example") # copy o my_file para o diretorio example, renameando: ./example/novoname

if __name__ == "__main__":
    copy_my_file("notes.txt")
~~~

## Movendo um arquivo

~~~python
import shutil    # biblioteca
def move_my_file(name_file):
    shutil.move(name_file, "./example")

if __name__ == "__main__":
    move_my_file("notes.txt")
~~~
