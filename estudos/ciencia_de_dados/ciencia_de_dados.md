# Ciência de Dados

## O que é Ciência de Dados? 

- A Ciência de Dados é o campo interdisciplinar que combina métodos estatísticos, programação e conhecimento de domínio para extrair informações valiosas e insights a partir de dados.
- Isso envolve uma série de atividades que vão desde a coleta de dados até a análise e a interpretação dos resultados para a tomada de decisões.

#### Ciência de Dados x Estatística x Machine Learning

- Embora relacionados, esses três campos não são idênticos:
    - Estatística foca na análise e interpretação dos dados e na inferência a partir deles.
    - Machine Learning (ML) é uma subárea da Inteligência Artificial que utiliza algoritmos para prever ou classificar dados com base em padrões aprendidos.
    - Ciência de Dados engloba ambos, usando estatística e ML para entender dados e resolver problemas complexos.

#### Aplicações

- Saúde: Identificação de padrões de doenças, previsão de surtos, personalização de tratamentos.
- Finanças: Previsão de riscos, detecção de fraudes, análise de crédito.
- Varejo e Marketing: Análise do comportamento de compra, segmentação de clientes, otimização de campanhas de marketing.
- Indústria: Otimização da cadeia de suprimentos, manutenção preditiva em equipamentos, automação de processos.
- Tecnologia e Internet: Recomendação de conteúdo, reconhecimento de imagens e voz, sistemas de busca.

#### Perfil do Cientista de Dados

- O Cientista de Dados é um profissional que atua na coleta, organização, análise e interpretação de dados.
- Para isso, ele precisa ter:
    - Habilidades em Programação: Proficiência em linguagens como Python e R, além de bibliotecas específicas (como Pandas e NumPy) para manipulação de dados.
    - Conhecimento de Estatística e Matemática: Estatística é a base para interpretar dados corretamente, permitindo a construção de modelos de aprendizado de máquina e análises complexas.
    - Mentalidade Analítica e de Solução de Problemas: Ser capaz de formular e responder a perguntas que guiem a análise de dados.
    - Comunicação e Storytelling: Explicar resultados técnicos de maneira acessível e convincente para tomadores de decisão.
    - Além disso, o cientista de dados precisa estar em constante aprendizado devido à rápida evolução das tecnologias e ferramentas na área.

## O Ciclo de Vida dos Dados

#### Coleta de Dados

- Na ciência de dados, o ciclo de vida dos dados é uma sequência de etapas essenciais que guiam o processo de trabalho com dados, desde sua coleta até a análise e modelagem. 
- A primeira etapa desse ciclo é a Coleta e Armazenamento de Dados, onde tudo começa.
- Coleta de dados é o processo de reunir informações que servirão como base para as análises. 
- É um passo crítico, pois a qualidade dos dados coletados afeta diretamente a precisão dos resultados de análise e das previsões que poderão ser feitas. 
- Dados de baixa qualidade, incompletos ou imprecisos podem levar a conclusões erradas.
- Métodos de Coleta de Dados Existem diversas formas de coletar dados, dependendo do objetivo e da natureza do projeto. 
- Alguns métodos incluem:
    - Questionários e pesquisas: Utilizados para coletar informações diretamente de indivíduos.
    - Sensores e dispositivos: Como câmeras, termômetros e outros dispositivos que captam dados automaticamente.
    - Web scraping: Uma técnica usada para extrair dados da internet, como reviews de produtos, notícias, ou dados de redes sociais.
    - Bases de dados públicas ou privadas: Muitas organizações disponibilizam bases de dados que podem ser usadas para análises, como dados governamentais, dados de saúde, entre outros.
- Cuidados na Coleta
    - Qualidade e confiabilidade: Certificar-se de que os dados são confiáveis e vêm de fontes verificadas.
    - Relevância: Focar em coletar dados relevantes para o problema que você quer resolver, evitando excesso de dados desnecessários.
    - Ética e privacidade: Respeitar as leis de proteção de dados e os direitos de privacidade dos indivíduos.

#### Armazenamento de Dados

- Após a coleta, os dados precisam ser armazenados de maneira segura e organizada. 
- Existem diferentes opções de armazenamento, que devem ser escolhidas conforme o tipo e o volume dos dados e os recursos da organização.
- Bancos de dados relacionais: Como MySQL e PostgreSQL, que organizam dados em tabelas e são ideais para dados estruturados.
- Bancos de dados não relacionais (NoSQL): Como MongoDB, que lidam bem com dados não estruturados ou semi-estruturados.
- Armazenamento em nuvem: Plataformas como AWS, Google Cloud e Azure oferecem espaço de armazenamento em servidores remotos, com a vantagem da escalabilidade e da segurança.
- Data Lakes: Uma opção para armazenar grandes volumes de dados brutos (não processados), comum em projetos de Big Data.
- Considerações no Armazenamento
    - Escalabilidade: O sistema precisa ser capaz de crescer conforme a quantidade de dados aumenta.
    - Segurança: Medidas de proteção de dados, como criptografia e controle de acesso, são essenciais para evitar vazamentos.
    - Facilidade de acesso e consulta: O armazenamento deve permitir acesso rápido e eficiente aos dados, facilitando o trabalho dos analistas.

#### Pré-processamento e Limpeza de Dados

- Após a coleta e o armazenamento dos dados, passamos para a fase de pré-processamento e limpeza. 
- Aqui, o objetivo é preparar os dados para análise, eliminando ruídos, inconsistências, ou erros que possam comprometer a precisão dos resultados.
- Importância do Pré-processamento
    - Dados brutos geralmente contêm inconsistências e elementos que podem distorcer ou limitar as análises. 
    - Pré-processar significa transformar esses dados em um formato mais estruturado, adequado e confiável para serem analisados. 
    - Esse processo permite que os modelos e algoritmos de ciência de dados trabalhem com informações precisas e, consequentemente, tragam resultados mais acurados.
- Etapas de Limpeza de Dados
    - A limpeza é um processo que envolve diversas etapas. 
    - Algumas das principais atividades nessa fase incluem:
        - Tratamento de valores nulos: Em muitos casos, parte dos dados estará ausente ou incompleta. É importante decidir o que fazer com esses valores:
            - Remover linhas ou colunas inteiras se muitos valores estiverem faltando.
            - Substituir valores nulos por uma média, mediana ou outro valor que faça sentido para o conjunto de dados.
        - Remoção de duplicatas: Muitas vezes, registros duplicados podem aparecer. Eles devem ser identificados e removidos, pois a duplicação pode enviesar os resultados.
        - Correção de inconsistências: Diferentes padrões de preenchimento de dados podem ocorrer, como variações nos nomes de categorias (ex.: “SP” e “São Paulo”). Essas discrepâncias precisam ser unificadas.
        - Filtragem de outliers: Valores fora do esperado ou fora do padrão podem ser considerados outliers e podem ser resultado de erros de entrada ou situações extremas. Devemos avaliar se faz sentido removê-los ou mantê-los.
- Transformação de Dados
    - Após a limpeza inicial, passamos para a transformação dos dados, que é essencial para adequar o conjunto de dados ao que será necessário nas etapas de análise e modelagem.
- Normalização e padronização
    - Alguns modelos de aprendizado de máquina se beneficiam se os dados numéricos estiverem em uma mesma escala. 
    - Normalização ajusta os valores para uma escala de 0 a 1, enquanto a padronização ajusta os dados para uma distribuição com média zero e desvio padrão um.
- Codificação de variáveis categóricas
    - Muitas análises e modelos exigem dados numéricos. 
    - Para transformar variáveis categóricas (como "cor", "estado" ou "gênero") em números, usamos técnicas como one-hot encoding, que cria colunas binárias para cada categoria.
- Criação de novas variáveis (feature engineering)
    - A criação de variáveis derivadas pode melhorar a análise. 
    - Por exemplo, se você tem a data de nascimento de clientes, você pode calcular a idade e adicionar essa variável, que pode ser mais útil na análise do que a própria data de nascimento.
- Ferramentas para Pré-processamento e Limpeza de Dados
    - Pandas (Python): Para manipulação e limpeza de dados em DataFrames.
    - NumPy (Python): Para operações numéricas e manipulação de matrizes.
    - OpenRefine: Software para limpeza de dados baseado em GUI, facilitando a detecção de inconsistências.
- Resumo
    - A fase de pré-processamento e limpeza de dados é fundamental para transformar os dados brutos em um conjunto de dados organizado, coerente e confiável. 
    - Com dados bem processados e limpos, as próximas etapas – como análise exploratória e modelagem – terão uma base sólida, o que aumentará a confiabilidade dos resultados.

#### Exploração e Análise Inicial dos Dados

- Após a coleta, armazenamento, pré-processamento e limpeza, a próxima etapa no ciclo de vida dos dados é a Exploração e Análise Inicial dos Dados. 
- Essa fase é conhecida como análise exploratória de dados (ou Exploratory Data Analysis - EDA) e é crucial para entender as principais características e padrões dos dados antes de avançar para análises e modelagens mais avançadas.
- A exploração e análise inicial dos dados é uma fase essencial para conhecer o conjunto de dados e identificar tendências, padrões e anomalias. Ela fornece insights valiosos que servirão como base para as próximas etapas, como a seleção de variáveis e a aplicação de modelos.
- A análise exploratória busca responder a perguntas importantes, como:
    - Como estão distribuídas as variáveis no conjunto de dados?
    - Existem padrões, tendências ou relações entre variáveis?
    - Há valores atípicos ou outliers que podem afetar a análise?
    - Os dados estão em uma escala apropriada, ou precisam de ajustes?
- Esse processo permite aos analistas compreender melhor os dados e tomar decisões informadas sobre quais técnicas e modelos podem ser aplicados com mais eficácia.
- Principais Técnicas de Análise Exploratória:
    - Estatísticas Descritivas: Avaliar métricas básicas, como média, mediana, moda, mínimos e máximos, variância e desvio padrão. Essas medidas ajudam a entender a dispersão e a centralidade dos dados, oferecendo uma primeira visão de como as variáveis estão distribuídas.
    - Distribuição de Frequência: Avaliar a frequência de valores para variáveis categóricas ou contínuas. Gráficos de barras e histogramas são frequentemente usados para visualizar como os valores de uma variável se distribuem.
    - Gráficos: Ferramentas de visualização são essenciais para a análise exploratória. Alguns dos gráficos mais comuns incluem:
        - Histogramas: Mostram a distribuição de uma variável numérica, facilitando a visualização de assimetrias e a identificação de outliers.
        - Boxplots (ou gráficos de caixa): Representam a distribuição de uma variável numérica, destacando os quartis e os valores extremos.
        - Scatter plots (ou gráficos de dispersão): Úteis para analisar a relação entre duas variáveis contínuas.
        - Matriz de correlação: Quando se trabalha com várias variáveis numéricas, a matriz de correlação mostra como cada variável se relaciona com as demais, ajudando a identificar correlações fortes ou fracas.
- Identificação de Padrões e Anomalias
    - Outliers: Esses são valores que se destacam de forma significativa em relação à maioria dos dados e podem resultar de erros ou representar casos excepcionais. É importante identificá-los e decidir se devem ser tratados ou excluídos.
    - Padrões e Correlações: Ao examinar a relação entre variáveis, podemos identificar correlações que podem guiar a modelagem futura. Por exemplo, uma forte correlação entre duas variáveis pode indicar que uma delas pode ser uma boa preditora para a outra.
- Ferramentas e Métodos Usados na Análise Inicial
    - Muitos cientistas de dados usam ferramentas como o Python (com bibliotecas como Pandas e Matplotlib) e o R para realizar essa análise. Algumas das funções principais envolvem:
        - .describe() em Pandas, que resume estatísticas descritivas para cada coluna numérica.
        - .corr() para calcular a matriz de correlação.
        - Funções de visualização como hist(), boxplot() e scatter() em Matplotlib e Seaborn, que ajudam a visualizar padrões e tendências.
- Interpretação e Conclusões Iniciais
        - A fase de análise inicial não só ajuda a identificar problemas ou características peculiares dos dados, mas também permite formular hipóteses que serão úteis na modelagem. Após realizar a análise exploratória, você deve ter um entendimento claro dos dados, incluindo:
            - Quais variáveis parecem ter uma relação mais forte e podem ser investigadas em análises mais detalhadas.
            - Quais transformações ou ajustes nos dados podem ser necessários antes de avançar para a modelagem.
