# Linux Commands

- Repositório criado para guardar comandos Linux.
- Todos os comandos aqui mostrados tem suas próprias bandeiras e parâmetros que podem receber.
- Para saber esses comandos basta digitar "man _nomedocomando_" ou "_nomedocomando_ --help"

## Sumário

- [Lista de Comandos](#lista-de-comandos)

  - [xdg-open](#xdg-open)
  - [mv](#mv)
  - [adicionando ou criando linhas em um arquivo](#adicionando-ou-criando-linhas-em-um-arquivo)
  - [less](#less)
  - [wc](#wc)
  - [sort](#)
  - [uniq](#uniq)

- [Comandos Complexos](#comandos-complexos)
- [Variáveis de Ambiente](#variaveis-de-ambiente)

## Lista de Comandos:

### xdg-open

- Abre o arquivo ou pasta dado como argumento;
- Exemplo:

```bash
  # abre a pasta no explorador de arquivos
  xdg-open .

  # abre o arquivo de acordo com o padrão
  xdg-open exemplo.pdf

  # tambem pode ser usado para abrir um site no navegador
  xdg-open 'https://google.com'
```

### mv

- move ou renomeia um determinado arquivo:
- Exemplo:

```bash
  # move um arquivo para uma pasta
  mv arquivo.pdf pasta

  # renomeia o arquivo
  mv arquivo.pdf novoarquivo.pdf
```

### adicionando ou criando linhas em um arquivo

- Exemplo:

```bash
  # apaga o conteudo do arquivo e adiciona o resultado de pwd em path.txt
  pwd > path.txt

  # adiciona o resultado de date em date.txt
  date >> date.txt
```

### less

- Mostra um arquivo de uma nova forma, da mesma forma que o manual
- Exemplo:

```bash
# mostra o conteudo deste arquivo
less arquivo.txt
```

### wc

- mostra a quantidade de linhas, palavras e bytes respectivament do arquivo dado
- Exemplo:

```bash
# mostra os dados da arquivo
wc arquivo.txt

# lista os arquivos e mostra os dados especificados acima
# por dedução a resposta será a quantidade de arquivos
ls -al | wc
```

### sort

- ordena os conteudos de um determinado arquivo
- Exemplo:

```bash
# ordena os conteudos do arquivo
sort palavras.txt

# ordena numericamente os numeros no arquivo
sort -n numeros.txt
```

### uniq

- junta as linhas que estejam juntas e repetidas
- Exemplo

```bash
  # nesse caso suponha que temos um arquivo com diversos sabores mas que podem ser repetidos
  # o comando irá juntar esses sabores iguais que estão repetidos e compactar em apenas uma única linha
  uniq flavors.txt
```

### find

- encontra um determinado arquivo de acordo com os parametros dados
- Exemplo:

```bash
# listando recursivamente os arquivos existentes em "."
find .

#  procurando no diretorio "." qualquer diretorio que tenha nome "*E*"
find . -type d -name "*.py"

```

### grep

- mostra todas as vezes que uma determinada palavra aparece em um arquivo
- Exemplo:
```bash
# mostra todas as vezes que "her" aparece em "lethergo.txt"
grep her lethergo.txt

# mostra as vezes que main aparece:
# - em todos os arquivos do diretorio;
# - mostrando o numero da linha que aparece;
# - mostrando as duas linhas antes e depois de cada aparicao
grep -rnC 2 "main" .
```

## Comandos Complexos

```bash
# 1. ordena o conteúdo do arquivo;
# 2. mixa de acordo com os repetidos e mostra a quantidade de repetições;
# 3. ordena por numero e de forma reversa
# 4. manda o resultado para o arquivo _data.xlsx_
sort flavors.txt | uniq -c | sort -nr > data.xlsx

# mostra todos os arquivos que tenham extensoes com duas letras
echo *.??

# remove os arquivos que tenham extensão ".txt"
rm *.txt

# criando arquivos a.txt, b.txt, c.txt
touch {a,b,c}.txt

# criando arquivos com o mesmo nome mas com extensoes diferentes
touch main.{py,js,html,css}
```

## Variaveis de Ambiente

```bash
echo $(nome_da_variavel)
```

- USER
- PATH
- SHELL
