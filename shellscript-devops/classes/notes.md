# Notes
Importante sempre iniciar o arquivo com BASH setado, exemplo:
```bash
#!/usr/bin/bash
```
ou
```bash
#!/bin/bash
```

E tambem sempre arrumar o permissionamento para que seja possivel executar o script, exemplo:
```bash
sudo chmod +x <script.sh>
```

Para executar o script, basta passar o comando ./ , exemplo:

```bash
./script.sh
```

Importante observar que sempre que executado um script, o bash abre uma nova sessao, logo, os comandos que nao sao nativos do shell, pode interferir na execucao do script. Uma boa pratica eh passar o binario do comando via variavel ambiente.