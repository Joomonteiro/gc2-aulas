## Executar o playbook do ansible para instalação do Nagios core e configuração
# Acesse a máquina em que o ansible se encontra instalado via ssh:

ssh vagrant@192.168.56.12

**o password é 'vagrant'

# Gerando chaves no nó de controle (onde o ansible se encontra)
ssh-keygen

# Copiando chaves para os nós gerenciados (managed nodes):
ssh-copy-id vagrant@192.168.56.<ip>

# Navege até a pasta com o playbook:
cd /vagrant_data
# Testando a conexão
ansible servers -i inventory -m ping
# Logo após rode o seguinte comando dentro da máquina:

ansible-playbook configurar-monitoramento.yml -i inventory
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

## Docs
Ansible 2.9.27 documentação:
https://docs.ansible.com/ansible/2.9/user_guide/basic_concepts.html

https://docs.ansible.com/ansible/2.9/index.html