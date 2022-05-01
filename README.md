# Tuberculosis-Classification

OBS: Caso o Github não renderize o arquivo .ipynb use os links abaixo:

- <a href="https://nbviewer.org/github/Julio-M39/01-Tuberculosis-Classification/blob/main/Primeira%20Etapa.ipynb">Primeira Etapa!</a> 
- <a href="https://nbviewer.org/github/Julio-M39/01-Tuberculosis-Classification/blob/main/Segunda%20Etapa.ipynb">Segunda Etapa!</a> 
- <a href="https://nbviewer.org/github/Julio-M39/01-Tuberculosis-Classification/blob/main/Terceira%20Etapa.ipynb">Terceira Etapa!</a> 

### Definição do Projeto

A radiografia de tórax tem um valor clínico importante no diagnóstico de doenças. Sendo a ferramenta de exame mais comum na prática médica. Assim, a detecção automática de doenças com base na radiografia de tórax se tornou um dos tópicos mais procurados na pesquisa de imagens médicas. A radiografia de tórax (ou radiografia torácica) é uma técnica de diagnóstico e imagem médica econômica e fácil de usar. Com papel importante o diagnóstico de doenças pulmonares. Radiologistas bem treinados usam raios-X do tórax para detectar doenças, como pneumonia, tuberculose e câncer de pulmão precoce. Em inglês é conhecido como Chest radiography (chest X-ray or CXR).

**Classificação de Tuberculose**

A tuberculose (TB) é a nona principal causa de morte no mundo e a principal causa de um único agente infeccioso, acima do HIV / AIDS. Globalmente, em 2016, a proporção de pessoas que desenvolveram tuberculose e morreram da doença (taxa de letalidade, CFR) foi de 16%, o que significa que cerca de 10,4 milhões de pessoas (90% adultos; 65% homens; 10% pessoas vivendo com HIV) adoeceu com TB.

Manifestações anormais de tuberculose frequentemente afetam a textura e a geometria dos pulmões nas radiografias, como consolidações e infiltrações, variando de padrões sutis a derrames óbvios. Abaixo uma imagem de pulmão com tuberculose:

<div>
<img src="https://user-images.githubusercontent.com/54995990/155441473-7e921109-44fd-47d8-8a83-669fb1a3f75d.png" width="300px" />
</div>

O objetivo desse projeto será treinar um modelo com imagens de pulmões saudáveis e com tuberculose para que o modelo seja capaz de fazer a classificação em novas imagens.

**Referências:**

<a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3876596/">Pulmonary tuberculosis as differential diagnosis of lung cancer</a>

<a href="https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1002686">Deep learning for chest radiograph diagnosis: A retrospective comparison of the CheXNeXt algorithm to practicing radiologists</a>

<a href="https://biomedical-engineering-online.biomedcentral.com/articles/10.1186/s12938-018-0544-y">Computer-aided detection in chest radiography based on artificial intelligence: a survey</a>

**Base de Imagens**

Os seguintes conjuntos de dados de imagem de radiografias de tórax (CXRs) estão disponíveis para a comunidade de pesquisa. Ambos os conjuntos contêm raios-X normais e anormais, com os últimos contendo manifestações de tuberculose.

**Conjunto de raios-X do Condado de Montgomery**: As imagens de raios-X deste conjunto de dados foram adquiridas no programa de controle da tuberculose do Departamento de Saúde e Serviços Humanos do Condado de Montgomery, MD, EUA. Este conjunto contém 138 radiografias póstero-anteriores, das quais 80 radiografias são normais e 58 radiografias são anormais com manifestações de tuberculose. Todas as imagens são anônimas e estão disponíveis no formato DICOM. O conjunto cobre uma ampla variedade de anormalidades, incluindo derrames e padrões miliares. O conjunto de dados inclui leituras de radiologia disponíveis como um arquivo de texto.

**Conjunto de raios X do Hospital de Shenzhen**: As imagens de raios X deste conjunto de dados foram coletadas pelo Hospital de Shenzhen em Shenzhen, providência em Guangdong, China. Os raios X foram adquiridos como parte dos cuidados de rotina no Hospital de Shenzhen. O conjunto contém imagens no formato JPEG. Existem 326 radiografias normais e 336 radiografias anormais, mostrando várias manifestações de tuberculose. 

Fonte de Dados:

https://lhncbc.nlm.nih.gov/publication/pub9931

### Etapas do Projeto

**Primeira Etapa:**

- Extração de informação dos datasets
- Ajustes, organização e união dos datasets
- Divisão em treinamento, validação e teste
- Criação de diretórios para armazenar as imagens
- Pré-processamento e aplicação de dataset augmentation (Geração de Imagens Sintéticas)
- Armazenamento das imagens 

**Segunda Etapa:**

- Criação do modelo
- Definição dos hiperparâmetros
- Criação da arquitetura
- Compilação
- Definição do checkpoint
- Definição do Reduce on Plateau
- Treinamento do modelo
- Curvas do aprendizado

**Terceira Etapa:**

- Carregamento do modelo
- Previsões nos dados de teste
- Matriz de confusão
- Relatório de classificação

### **Resultados**

Para os resultados, plotamos uma matriz e um relatório de classificação que podem ser visto na imagem abaixo:

<div>
<img src="https://user-images.githubusercontent.com/54995990/166153386-2f043e6d-1401-4647-a61f-a4b5277d21a0.png" width="980px" />
</div>

No geral, o modelo apresenta um bom equilíbrio, embora ainda tenhamos espaço para melhorias. O modelo pode ser melhorado com uma otimização dos parâmetros utilizados na rede, modificações na arquitetura da rede e aplicação de pré-processamento nas imagens.
