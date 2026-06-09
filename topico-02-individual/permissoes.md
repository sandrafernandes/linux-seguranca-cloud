# Permissoes aplicadas
## Ambiente utilizado
Linux no browser.
## Utilizador e grupos
Foram utilizados os comandos whoami, id e groups para identificar o utilizador atual e os grupos associados.
root@ubuntu:~/topico-02-individual$ whoami
root
root@ubuntu:~/topico-02-individual$ id
uid=0(root) gid=0(root) groups=0(root)
root@ubuntu:~/topico-02-individual$ groups
root
## Ficheiros criados
publico.txt
restrito.txt
script.sh
## Permissoes aplicadas
Ficheiro	Permissao	Justificacao
publico.txt	644     	Permite leitura publica e escrita apenas ao proprietario.
restrito.txt	640     	Restringe o acesso de outros utilizadores.
script.sh	u+x	        Permite execucao apenas ao utilizador proprietario.
Relacao com o principio do menor privilegio
As permissoes foram definidas para permitir apenas os acessos necessarios a cada ficheiro. Isto reduz riscos de alteracoes indevidas e aumenta a seguranca do sistema.
