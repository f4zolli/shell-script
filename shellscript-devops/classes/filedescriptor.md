# EXPLORANDO UM FILE DESCRIPTOR
 ```bash
 man bash
 /<> # Opening file descriptors for reading and writing
```
```bash
 exec 8<> teste_file_descriptor.txt # executando (setando) file descriptor
```
```bash
 fuser -v teste_file_descriptor.txt # investigar o arquivo (qual processo esta ligado e afins), retorna o processo do bash
```
 No diretorio /proc podemos identificar o processo do bash pelo ID e no /proc/<id_bash>/fdinfo haverá o file descriptor que setamos.
 
 Se abrirmos o file descriptor com o cat, exemplo:
 ```bash
 cat 8 # file descriptor que haviamos setado anteriormente
```
 Haverá algumas informações no retorno, e a mais importante é a "pos:", que eh a posicao de onde o arquivo sera lido.

 Inserindo informacao no arquivo do file descriptor:
```bash
 echo "1- testando a escrita" >&8
 ```

 Fechando file descriptor
 ```bash
 exec <&8-
 ```

