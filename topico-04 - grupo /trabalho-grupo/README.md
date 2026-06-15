# Topico 4 - PPlano de segurança inicial para um serviço web publicado

## Ambiente utilizado
Linux no browser.

## Objetivo desta atividade
Não é fazer hardening avançado, mas definir medidas iniciais coerentes para reduzir a superfície de ataque.

## Servico analisado
Cenário escolhido: HTML com Nginx
Descrição: Foi publicado um pequeno site estático desenvolvido em HTML e CSS através do servidor web Nginx.


## Estrutura criada
Foi criada uma estrutura de diretorios para organizar os ficheiros do modulo.

## 3. Superfície de ataque

Elemento Exposto	                             | Risco	Necessário?     |	Medida proposta
SSH	Acesso não autorizado	                        Sim	                      Limitar o acesso a utilizadores autorizados
HTTP	Tráfico sem encriptação	                    Não	                       Redirecionar para HTTPS
HTTPS	Exploração de vulnerabilidades web	        Sim	                      Utilizar certificado SSL válido
Base de dados	Exposição de dados	                Não	                      Não expor externamente
Diretório web	Divulgação de ficheiros sensíveis	Sim	                      Aplicar permissões adequadas
WordPress admin	Ataques de autenticação	            Não	                       Não utilizado


## 4. Regras de firewall propostas

Serviço	      | Porta   | Decisão	   | Justificação
SSH       	    22	      Aberta	     Permitir administração remota
HTTP	        80	      Aberta	     Permitir direcionamento para HTTPS
HTTPS	        443	      Bloqueado	     Não configurado
MariaDB/MySQL	3306	  Bloqueado	     Não utilizamos

## 5. Medidas de hardening inicial

1. Atualização regular do sistema
Executar atualizações de segurança regularmente.

sudo apt update
sudo apt upgrade

2. Rever serviços ativos
Desativar serviços não necessários.

systemctl list-units --type=service

3. Aplicar firewall
Permitir apenas os serviços necessários.

4. Rever permissões do diretório web
Garantir que apenas utilizadores autorizados podem modificar ficheiros.

/var/www/html/

5. Evitar utilização da conta root
Utilizar contas normais com privilégios sudo.

6. Proteger acessos remotos
Restringir o acesso SSH e monitorizar tentativas de ligação.

## 6. Plano de validação

Validação	                     | Como fazer	       | Resultado esperado.              | Evidência
Estado da firewwall	               Sudo ufw status.      Firewall activo	                Output do comando/ print de ecrã
Serviço web acessível	           Navegador / curl	     Visualização de página.            Output do comando/ print de ecrã
SSH disponível	                   Ssh utilizador@ip	 Ligação estabelecida	            Output do comando/ print de ecrã
Portas desnecessárias fechadas	   ss  -tulpn	         Apenas portas necessárias abertas	Output do comando/ print de ecrã


## 7. Link do repositório GitHub


## 8. Conclusão

O grupo definiu medidas básicas de segurança para reduzir riscos associados à publicação de um serviço web em Linux. As ações propostas permitem proteger o servidor, controlar acessos e preparar futuras melhorias, como a implementação de HTTPS e monitorização contínua.

## Evidencias

![nginx](evidencias/instalar_nginx.png)

![nginx](evidencias/start_nginx.png)

![ufw](evidencias/verificar_status_ufw.png)

![ufw](evidencias/regras_ufw.png)

![lynis](evidencias/instalar_lynis.png)

![lynis](evidencias/instalar_lynis1.png)

![lynis](evidencias/lynis_instalado2.png)

![gardening](evidencias/gardening_atualizar_pacotes.png)

![gardening](evidencias/gardening_servicos_ativos.png)

![gardening](evidencias/gardening_portas_abertas.png)