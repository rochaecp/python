# Conda

- Gerenciador de pacotes (biblitoecas) que possuem módulos (arquivos .py)
- Gerenciador de ambientes (permite criar ambiente e instalar bibliotecas nele)
- Conda-forge
    - Coleção de pacotes mantidos pelos usuários
    - Pacotes: anaconda.org
    
# Anaconda

- É um instalador completo do conda

# Miniconda

- Versão reduzida do Anaconda
- Abrir o prompt do miniconda
    - (base): ambiente base (padrão)

## Vídeos

- [Install Miniconda (Python) with Jupyter Notebook and Setting Up Virtual Environments on Windows 10](https://www.youtube.com/watch?v=XCvgyvBFjyM)

## Comandos Diversos

~~~bash
python # exibe versão do python e abre console para digitar comandos, exit() para sair
where python # local onde o python esta instalado
~~~

## Listar os ambientes virtuais criados na máquina

~~~bash
conda env list
~~~

## Criar um ambiente virtual

~~~bash
conda create -n nomeAmbiente python # utilizando a versão mais recente do python do ambiente
~~~

~~~bash
conda create -n nomeAmbiente python=3.7 # alterando a versão do python
~~~

## Ativar um ambiente virtual

~~~bash
conda activate nomeAmbiente python
~~~

## Desativar um ambiente virtual

~~~bash
conda deactivate
~~~

## Instalar um pacote / programa no ambiente virtual

~~~bash
pip install pandas # versão mais recente
~~~

~~~bash
pip install pandas==0.19.2 # uma versão especifica
~~~

~~~bash
conda install jupyter notebook
~~~

## Desinstalar um pacote / programa no ambiente virtual

~~~bash
conda uninstall cuda90
~~~