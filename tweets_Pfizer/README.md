Coleta de tweets recentes sobre a vacina Pfizer & BioNTech.

Os dados são coletados usando o pacote tweepy Python para acessar a API do Twitter.

https://www.kaggle.com/gpreda/pfizer-vaccine-tweets

Durante a escrita do codigo foi encontrado um erro que na veideo aula deu certo, porém, quando executado aqui não deu

<code>
df= df.join( pd.concat(( getattr( df['date'], i).rename(i) for i in L), axis=1))
</code>

Como ela não deu certo por meio do for, resolvi fazer linha por linha com base no algoritmo encontrado no seguinte link:

https://stackoverflow.com/questions/25146121/extracting-just-month-and-year-separately-from-pandas-datetime-column


<code>
df['year'] = pd.DatetimeIndex(df['date']).year
df['month'] = pd.DatetimeIndex(df['date']).month
df['day'] = pd.DatetimeIndex(df['date']).day
df['dayofweek'] = pd.DatetimeIndex(df['date']).dayofweek
df['dayofyear'] = pd.DatetimeIndex(df['date']).dayofyear
df['weekofyear'] = pd.DatetimeIndex(df['date']).weekofyear
df['quarter'] = pd.DatetimeIndex(df['date']).quarter
 </code>



# Bibliotecas
##manipulação dos dados
### Pandas


##visualização dos dados
### missingno
### matplotlib
### seaborn


## Expressoes regulares
### Python RegEx
Um RegEx, ou Expressão Regular, é uma sequência de caracteres que forma um padrão de pesquisa. RegEx pode ser usado para verificar se uma string contém o padrão de pesquisa especificado.

Função | Descrição
--------- | ------
sub     | Replaces one or many matches with a string

	
https://www.w3schools.com/python/python_regex.asp
