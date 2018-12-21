
# Importar o DataSet Titanic


```python
#importar o arquivo para uma variavel
titanic_csv = open('titanic.csv','r')
```


```python
# o metodo readlines identifica cada linha atravez do \n 
titanic_csv.readlines()
```

    ['PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n',
     '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n',
     '2,1,1,"Cumings, Mrs. John Bradley (Florence Briggs Thayer)",female,38,1,0,PC 17599,71.2833,C85,C\n',
     '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n',
     '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n',
     '5,0,3,"Allen, Mr. William Henry",male,35,0,0,373450,8.05,,S\n',
     '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n',
     '7,0,1,"McCarthy, Mr. Timothy J",male,54,0,0,17463,51.8625,E46,S\n',
     '8,0,3,"Palsson, Master. Gosta Leonard",male,2,3,1,349909,21.075,,S\n',
     '9,1,3,"Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)",female,27,0,2,347742,11.1333,,S\n',
     '10,1,2,"Nasser, Mrs. Nicholas (Adele Achem)",female,14,1,0,237736,30.0708,,C\n',
     '891,0,3,"Dooley, Mr. Patrick",male,32,0,0,370376,7.75,,Q\n']

```python
#posicionar o cursor na linha 0
titanic_csv.seek(0)
```




    0




```python
#lendo o arquivo e jogando na variavel
linhas = titanic_csv.readlines()
```


```python
linhas
```




    ['PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n',
     '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n',
     '2,1,1,"Cumings, Mrs. John Bradley (Florence Briggs Thayer)",female,38,1,0,PC 17599,71.2833,C85,C\n',
     '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n',
     '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n',
     '5,0,3,"Allen, Mr. William Henry",male,35,0,0,373450,8.05,,S\n',
     '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n',
     '7,0,1,"McCarthy, Mr. Timothy J",male,54,0,0,17463,51.8625,E46,S\n',
     '8,0,3,"Palsson, Master. Gosta Leonard",male,2,3,1,349909,21.075,,S\n',
     '9,1,3,"Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)",female,27,0,2,347742,11.1333,,S\n',
     '10,1,2,"Nasser, Mrs. Nicholas (Adele Achem)",female,14,1,0,237736,30.0708,,C\n',
     '891,0,3,"Dooley, Mr. Patrick",male,32,0,0,370376,7.75,,Q\n']




```python
linhas[0]
```
    'PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked\n'

```python
linhas[1]
```




    '1,0,3,"Braund, Mr. Owen Harris",male,22,1,0,A/5 21171,7.25,,S\n'




```python
linhas[3]
```




    '3,1,3,"Heikkinen, Miss. Laina",female,26,0,0,STON/O2. 3101282,7.925,,S\n'




```python
linhas[4]
```




    '4,1,1,"Futrelle, Mrs. Jacques Heath (Lily May Peel)",female,35,1,0,113803,53.1,C123,S\n'




```python
titanic_csv.close()
```


```python
linhas[0].split(',')
```




    ['PassengerId',
     'Survived',
     'Pclass',
     'Name',
     'Sex',
     'Age',
     'SibSp',
     'Parch',
     'Ticket',
     'Fare',
     'Cabin',
     'Embarked\n']




```python
colunas = linhas[0].split(',') #vira uma lista de str
```


```python
colunas
```




    ['PassengerId',
     'Survived',
     'Pclass',
     'Name',
     'Sex',
     'Age',
     'SibSp',
     'Parch',
     'Ticket',
     'Fare',
     'Cabin',
     'Embarked\n']




```python
colunas[0]
```




    'PassengerId'




```python
colunas[1]
```




    'Survived'




```python
colunas[2]
```




    'Pclass'




```python
#cada coluna será um chave e os valores uma lista do dicionario
dados = linhas[1].split(',')
```


```python
print(colunas)
print(dados)
```

    ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']
    ['1', '0', '3', '"Braund', ' Mr. Owen Harris"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    


```python
i = 4
print(colunas[i])
print(dados[i])
```

    Sex
     Mr. Owen Harris"
    


```python
#deu ruim
print(len(colunas), len(dados))
```

    12 13
    

### Expressão Regular, vamos tirar a virgula e inverter o nome.


```python
def tratar_nome(linha):
    import re 
    match = re.compile(r'"(.*)(,)(\s.*)"')
    return match.sub(r'"\3 \1"', linha)   
```


```python
tratar_nome(linhas[1])
```




    '1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S\n'




```python
linha1_tratada = tratar_nome(linhas[1])
linha1_separada = linha1_tratada.split(",")
print(colunas)
print(linha1_tratada)
print(linha1_separada)
```

    ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']
    1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S
    
    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    


```python
titanic_dados = {}

for coluna in colunas:
    titanic_dados[coluna] = []
titanic_dados
```




    {'PassengerId': [],
     'Survived': [],
     'Pclass': [],
     'Name': [],
     'Sex': [],
     'Age': [],
     'SibSp': [],
     'Parch': [],
     'Ticket': [],
     'Fare': [],
     'Cabin': [],
     'Embarked\n': []}




```python
linhas[6]
```




    '6,0,3,"Moran, Mr. James",male,,0,0,330877,8.4583,,Q\n'




```python
#Tratando todas as linhas do data set

for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    print(dado_tratado)
```

    1,0,3," Mr. Owen Harris Braund",male,22,1,0,A/5 21171,7.25,,S
    
    2,1,1," Mrs. John Bradley (Florence Briggs Thayer) Cumings",female,38,1,0,PC 17599,71.2833,C85,C
    
    3,1,3," Miss. Laina Heikkinen",female,26,0,0,STON/O2. 3101282,7.925,,S
    
    4,1,1," Mrs. Jacques Heath (Lily May Peel) Futrelle",female,35,1,0,113803,53.1,C123,S
    
    5,0,3," Mr. William Henry Allen",male,35,0,0,373450,8.05,,S
    
    6,0,3," Mr. James Moran",male,,0,0,330877,8.4583,,Q
    
    7,0,1," Mr. Timothy J McCarthy",male,54,0,0,17463,51.8625,E46,S
    
    8,0,3," Master. Gosta Leonard Palsson",male,2,3,1,349909,21.075,,S
    
    9,1,3," Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson",female,27,0,2,347742,11.1333,,S
    
    10,1,2," Mrs. Nicholas (Adele Achem) Nasser",female,14,1,0,237736,30.0708,,C
 
    891,0,3," Mr. Patrick Dooley",male,32,0,0,370376,7.75,,Q
    
    


```python
#criando uma lista
for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    dado_como_lista = dado_tratado.split(',')
    print(dado_como_lista)
```

    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    ['2', '1', '1', '" Mrs. John Bradley (Florence Briggs Thayer) Cumings"', 'female', '38', '1', '0', 'PC 17599', '71.2833', 'C85', 'C\n']
    ['3', '1', '3', '" Miss. Laina Heikkinen"', 'female', '26', '0', '0', 'STON/O2. 3101282', '7.925', '', 'S\n']
    ['4', '1', '1', '" Mrs. Jacques Heath (Lily May Peel) Futrelle"', 'female', '35', '1', '0', '113803', '53.1', 'C123', 'S\n']
    ['5', '0', '3', '" Mr. William Henry Allen"', 'male', '35', '0', '0', '373450', '8.05', '', 'S\n']
    ['6', '0', '3', '" Mr. James Moran"', 'male', '', '0', '0', '330877', '8.4583', '', 'Q\n']
    ['7', '0', '1', '" Mr. Timothy J McCarthy"', 'male', '54', '0', '0', '17463', '51.8625', 'E46', 'S\n']
    ['8', '0', '3', '" Master. Gosta Leonard Palsson"', 'male', '2', '3', '1', '349909', '21.075', '', 'S\n']
    ['9', '1', '3', '" Mrs. Oscar W (Elisabeth Vilhelmina Berg) Johnson"', 'female', '27', '0', '2', '347742', '11.1333', '', 'S\n']
    ['10', '1', '2', '" Mrs. Nicholas (Adele Achem) Nasser"', 'female', '14', '1', '0', '237736', '30.0708', '', 'C\n']
    ['891', '0', '3', '" Mr. Patrick Dooley"', 'male', '32', '0', '0', '370376', '7.75', '', 'Q\n']
    

### Tratanto Listas


```python
dados_tratados = []

for dado in linhas[1:]:
    dado_tratado = tratar_nome(dado)
    dado_como_lista = dado_tratado.split(',')
    dados_tratados.append(dado_como_lista)

```


```python
print(dados_tratados[0][3])
```

    " Mr. Owen Harris Braund"
    


```python
# 1 - Pego cada linha da variavel dados_tratados e coloco em passageiro
# 2 - faço um for em passageiro e pego o indice e o restante dos dados
# 3 - vou na variavel coluna e pego a coluna no respectivo indice
for passageiro in dados_tratados:
    print(passageiro)
    for indice, dado in enumerate(passageiro):
        print(indice,dado)
    print("----------------------------")
```

    ['1', '0', '3', '" Mr. Owen Harris Braund"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']
    0 1
    1 0
    2 3
    3 " Mr. Owen Harris Braund"
    4 male
    5 22
    6 1
    7 0
    8 A/5 21171
    9 7.25
    10 
    11 S
    
    ----------------------------
    ['2', '1', '1', '" Mrs. John Bradley (Florence Briggs Thayer) Cumings"', 'female', '38', '1', '0', 'PC 17599', '71.2833', 'C85', 'C\n']
    0 2
    1 1
    2 1
    3 " Mrs. John Bradley (Florence Briggs Thayer) Cumings"
    4 female
    5 38
    6 1
    7 0
    8 PC 17599
    9 71.2833
    10 C85
    11 C
    
    ----------------------------
    

## linhas = Todo o arquivo, sem nenhum tratamento, onde cada indice é linha, por exemplo linha[0]

## colunas = ['PassengerId', 'Survived', 'Pclass', 'Name', 'Sex', 'Age', 'SibSp', 'Parch', 'Ticket', 'Fare', 'Cabin', 'Embarked\n']

## dados =['1', '0', '3', '"Braund', ' Mr. Owen Harris"', 'male', '22', '1', '0', 'A/5 21171', '7.25', '', 'S\n']

## titanic_dados = o dicionario com as chaves (colunas) sem os valores



```python
for passageiro in dados_tratados:
    for indice, dado in enumerate(passageiro):
        coluna = colunas[indice]
        titanic_dados[coluna].append(dado)
```


```python
titanic_dados["Age"][0]
```
    '22'
```python
for dado in titanic_dados["Age"]:
    print(dado)
```
    22
    38
    26
    35
    35
```python
##converter idade em float e se estiver ausente, será -1
for indice, age in enumerate(titanic_dados["Age"]):
    if titanic_dados['Age'][indice] != '':
        titanic_dados['Age'][indice] = float(age)
    else:
        titanic_dados['Age'][indice] = -1
```


```python
print(max(titanic_dados['Age']))
```

    80.0
    


```python
print(min(titanic_dados['Age']))
```

    -1
    


```python
#Copiar todas as idades, exceto -1
lista_idade = []

for idade in titanic_dados["Age"]:
    if idade != -1:
        lista_idade.append(idade)
    
```


```python
def media(lista):
    soma_total  = sum(lista)
    quantidade = len(lista)
    return soma_total / quantidade

```


```python
print(media(lista_idade))
```

    29.69911764705882
    


```python
media_idade = media(lista_idade)
```


```python
for indice, age in enumerate(titanic_dados['Age']):
    if age == -1:
        titanic_dados['Age'][indice] = media_idade
```

# Agora vamos fazer tudo o que executamos acima em apenas 3 linhas #Pandas \o/


```python
#Importando Pandas
```


```python
import pandas

titanic_dados = pandas.read_csv('titanic.csv')
titanic_dados.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>NaN</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>0</td>
      <td>3</td>
      <td>Palsson, Master. Gosta Leonard</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>349909</td>
      <td>21.0750</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>347742</td>
      <td>11.1333</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>Nasser, Mrs. Nicholas (Adele Achem)</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>237736</td>
      <td>30.0708</td>
      <td>NaN</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


```python

```
