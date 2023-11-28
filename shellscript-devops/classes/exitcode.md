# EXIT CODES
No exit code, definimos qual sera o codigo de saida. Se a pipeline/script executou ou nao com erro.
**EXIT CODE** = 0  -> SUCESSO
**EXIT CODE** ≠ 0  -> FALHA

Uma boa pratica, eh definir os exit codes para as falhas. Exemplo:
Caso o script tenha dado uma falha por questao A, o exit code definido para saida eh o 123.

O comando ***curl*** , tem toda a explicacao dos seus respectivos exit codes, dentro do manual.

```bash
man curl
/exit code # filtrar por exit code no manual do curl
```

OUTRA MANEIRA DE VERIFICAR EXIT CODE
```bash
echo $? # A saida eh o ultimo comando executado
```