# Análise de Logs

## Logs consultados

### journalctl

Comando:
journalctl -n 20

Finalidade:
Consultar eventos recentes do sistema.

### access.log

Comando:
sudo tail -n 20 /var/log/nginx/access.log

Finalidade:
Verificar acessos ao serviço web.

### error.log

Comando:
sudo tail -n 20 /var/log/nginx/error.log

Finalidade:
Identificar erros do Nginx.

## Evento relevante identificado

Foi registado um acesso ao serviço web através do navegador e através do comando curl localhost.
