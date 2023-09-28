# Sobre

Assembler para o conjunto de instruções hipotético usado na disciplina de Arquitetura de Computadores do IFPR-Paranavaí.

# Compilando

Para compilar, apenas use o **make**.

# Running

O binário do compilador é o **pasm**.

# Sobre o conjunto de instruções

A especificação do conjunto de instruções pode ser consultada na aula que ministro, 
em **docs/12-instrucoes-codificacao.pdf**.

Importante apenas ressaltar os seguintes pontos:
- 8 registradores de propósito geral
- Os registradores são de 16 bits
- Cada palavra da memória também tem 16 bits, de forma que o endereço 0 (zero) 
referencia os bytes 0 e 1, o endereço 1 referencia os bytes 2 e 3, e assim por diante.

# Sobre o código gerado

O linker irá buscar pelo símbolo **_start**, que deverá referenciar a instrução inicial do código.

O início do código gerado ficará da seguinte forma:

- Endereço 0 (zero): conterá o valor 0 (zero)

- Endereço 1: conterá uma instrução jump para o símbolo **_start**

Dessa forma, um simulador para tal arquitetura deverá setar como endereço inicial do registrador **pc** o endereço **1**.


# RODANDO O PROJETO

Para rodar o projeto antes temos que
Caso seja a primeira vez, deve realizar a compilação dos arquivos asm para .bin, neste repositório já estão compilados.
O comando para compilar é Make e deve ser realizado na pasta raíz do projeto.

Para rodar o projeto deverá ser o comando: python2 pysim.py
 

# Comandos:

*shutdown*: Encerrar o sistema.
*jobs*: Atividades em andamento no sistema.
*start*: Roda a função requisitada em um novo processo
**start print.bin**
*shut {job}* -> Encerra o processo
**shut print.bin**