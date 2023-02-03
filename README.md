# Linux Commands
- Repositório criado para guardar comandos Linux.
- Todos os comandos aqui mostrados tem suas próprias bandeiras e parâmetros que podem receber.
- Para saber esses comandos basta digitar "man _nomedocomando_" ou "_nomedocomando_ --help"
## Lista de Comandos:

- xdg-open

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

- mv

  - move ou renomeia um determinado arquivo:
  - Exemplo:
  ```bash
    # move um arquivo para uma pasta
    mv arquivo.pdf pasta

    # renomeia o arquivo
    mv arquivo.pdf novoarquivo.pdf
  ```

- adicionando ou criando linhas em um arquivo

  - Exemplo:
  ```bash
    # apaga o conteudo do arquivo e adiciona o resultado de pwd em path.txt
    pwd > path.txt

    # adiciona o resultado de date em date.txt
    date >> date.txt
  ```

