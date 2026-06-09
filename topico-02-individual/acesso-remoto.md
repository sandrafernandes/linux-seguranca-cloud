# Acesso remoto por SSH
## O que e SSH?
SSH (Secure Shell) - um protocolo de rede utilizado para aceder remotamente a servidores e sistemas Linux de forma segura atraves do terminal. A comunicação ée cifrada, protegendo os dados transmitidos entre o cliente e o servidor.
## Informacao seria necessaria para aceder a um servidor por SSH:
Utilizador:
root
Endereço IP:
172.30.1.2
Porta:
22
alavra-passe ou chave:
Palavra-passe do utilizador ou chave SSH configurada no servidor.
## Exemplo de comando de ligacao
ssh root@172.30.1.2
## Limitacao encontrada
Foi possivel identificar o utilizador e o endereço IP do ambiente Linux utilizado atraves dos comandos whoami e hostname -I.
No entanto, nao foi possivel validar uma ligação SSH remota completa, uma vez que o ambiente Linux no browser possui limitações de rede e não está configurado como um servidor SSH acessivel externamente.
##Evidencias recolhidas
Comandos executados:
whoami
hostname -I
Resultados obtidos:

Utilizador: root
Endereço IP: 172.30.1.2
