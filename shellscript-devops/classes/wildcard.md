# WILDCARD  
Sao caracteres que podem representar nomes genericos para arquivos e diretorios na linha de comando, por exemplo:
```bash
* = pode ser utilizado para representar TUDO
? = pode ser utilizado para representar um caracter/digito
$ = representa uma variavel
'exemplo R$3.00' = aspas simples, interepreta tudo como uma string
"exemplo R.00" = interpreta tudo como uma string, porem permite a substituicao de comando, ou seja, utiliza variavel
```

### Wildcards examples:
```bash
echo "O valor eh de R$3.00"  # Observamos que o numero 3 se torna uma variavel, por conta do dolar dentro das aspas duplas
```
```bash
echo 'O valor eh de R$3.00' # Observamos que o numero 3 NAO se torna uma variavel, pois esta dentro de uma aspas simples
```
```bash
echo "O valor eh de R\$3.00" # Observamos que por conta da barra invertida, o 3 nao se torna uma variavel
```
```bash
ls -l `which ls` # substituindo comando
```
```bash
ls *.txt # wildcard no qual utilizamos para pegar todos arquivos que sejam txt
```
```bash
ls ???????.txt # wildcard que pega qualquer arquivo que tenha 7 caracteres e seja do formato .txt
```
```bash
touch arq{1,2,3,4,5}.txt #wildcard bracket, utilizado para fazer mais de uma acao ao mesmo tempo
```