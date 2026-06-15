# Hardening Inicial

## Serviço Publicado

Nginx com página HTML estática.

## Riscos Específicos

* Acesso indevido ao servidor.
* Alteração dos ficheiros publicados.
* Exposição de serviços desnecessários.

## Medidas Aplicáveis Agora

1. Atualizar pacotes do sistema.
2. Utilizar firewall.
3. Rever permissões em /var/www/html.
4. Utilizar palavras-passe fortes.
5. Evitar utilização direta do utilizador root.
6. Manter apenas serviços necessários ativos.

## Medidas para Tópicos Seguintes

* Implementação de HTTPS.
* Monitorização de logs.
* Backups automáticos.
* Hardening avançado do Nginx.
