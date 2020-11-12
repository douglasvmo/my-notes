# Swap

> coisas interessantes sobre a area de troca do linux

## Arquivo de swap
Criando um arquivo de troca de 1gb a partir da partição /dev/sda2.
```bash
# dd if=/dev/sda2 of=/swapfile bs=1G count=1
```
* comando **dd**, iniciais para Data Definition que tem como função converter e copiar arquivos.
* argumento **if**, input file, ou seja  arquivo de entrada.
* argumento **of**, output file, ou seja  arquivo de saida.
* argumento **bs**, block size, obviamente o tamanho do bloco para swap.
* argumento **count**, contador, multiplica a quantidade de block size(bs).