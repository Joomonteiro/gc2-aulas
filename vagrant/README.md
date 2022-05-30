## Como visualizar os dados coletados

## Acessar o nagios no seguinte endereço

`http://192.168.56.ip/nagios/`

**Obs Substitua 'ip' pelo o ip da máquina

## NetData 

## Abrir o navegador no seguinte link

`http://192.168.56.ip/nagios/`

**Obs Substitua 'ip' pelo o ip da máquina

## Comandos úteis para o net data e o nagios

## test de estresse da cpu
stress-ng
sudo apt install stress-ng
stress-ng --cpu 8 --io 4 --vm 2 --vm-bytes 128M --fork 4 --timeout 120s

## teste de envio de e-mails do NetData já configurado
sudo su -s /bin/bash netdata
/usr/libexec/netdata/plugins.d/alarm-notify.sh test