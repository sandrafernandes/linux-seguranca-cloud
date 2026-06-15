# Plano de Continuidade Operacional

## Serviço crítico

Nginx

## Ficheiros críticos

* /var/www/html/index.html
* /etc/nginx/nginx.conf

## Logs importantes

* /var/log/nginx/access.log
* /var/log/nginx/error.log
* journalctl

## Periodicidade de Backup

### Conteúdo Web

Semanal

### Configuração do Nginx

Após cada alteração

### Documentação

Mensal

## Procedimento de Recuperação

1. Identificar a falha.
2. Verificar o estado do serviço.
3. Restaurar os ficheiros a partir do backup.
4. Reiniciar o Nginx.
5. Validar através do navegador ou curl.

## Critérios de Validação

* O Nginx encontra-se ativo.
* A página web abre corretamente.
* Não existem erros nos logs.
* O conteúdo recuperado corresponde ao original.
