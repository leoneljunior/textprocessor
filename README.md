# GET Started

1. Execute o console.

2. Entre no diretório "/source" desse projeto.

3. Execute esse comando "python JSONTextProcess.py /SEUDIRETORIO/arquivo.json"

4. Irá aparecer um menu, digite 1 no terminal e aperte ENTER.

5. Um Arquivo será gerado na pasta source nominado como "tweets_data-atual.tsv"


## obs:

* Você pode configurar o formato do arquivo de entrada na função Split(Linha 16) mudando a variável delimiters.

* Na função "processTwitterText()" você terá que selecionar texto a ser processado e colocar na variável "text".

## Exemplo:

imput_file.txt

```txt
324234, TEXTO A SER PROCESSADO 1, -123.213, 125.234
765666, TEXTO A SER PROCESSADO 2, -133.213, 122.234
655634, TEXTO A SER PROCESSADO 3, -25.213, 125.234
763487, TEXTO A SER PROCESSADO 4, -223.213, 125.234
```

A Função split irá ficar assim:

```python
def split(string, maxsplit=0):
    delimiters = ","
    import re
    regexPattern = '|'.join(map(re.escape, delimiters))
    return re.split(regexPattern, string, maxsplit)  
```

E na função "processTwitterText()" irá ficar assim:
