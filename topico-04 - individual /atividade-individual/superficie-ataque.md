# Superfície de Ataque

## Serviço Web Utilizado

Nginx com página HTML estática publicada no Tópico 3.

## Serviços Observados

* SSH
* Nginx

## Portas Observadas

* 22/TCP (SSH)
* 80/TCP (HTTP)

## Portas Necessárias

* Porta 22 para administração remota.
* Porta 80 para acesso ao serviço web.

## Riscos Identificados

1. Acesso não autorizado através de SSH.
2. Alteração indevida dos ficheiros do site.
3. Exposição de serviços desnecessários.
