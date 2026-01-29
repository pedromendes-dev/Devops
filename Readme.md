# Vagrant - Guia de Comandos

## Conceitos Básicos
O Vagrant chama as imagens (ISO) de **Box** (caixas).

## Comandos Principais

### Gerenciamento de VMs
- `vagrant up` - Roda/sobe a máquina virtual
- `vagrant halt` - Desliga a máquina virtual
- `vagrant destroy -f` - Destrói a máquina virtual (force)
- `vagrant status` - Verifica o status das VMs
- `vagrant ssh <nome>` - Conecta via SSH na VM

### Verificação de Rede
Para verificar se o IP foi configurado corretamente:
```bash
vagrant ssh server1 -c "ip -c a show enp0s8"
```
> **Nota:** `enp0s8` é o padrão para máquinas Ubuntu.

## Estrutura do Projeto
```
infra/
  ubuntu/       - Configuração Vagrant para Ubuntu
  Windows10/    - Configuração Vagrant para Windows 10
Test/           - Ambiente de testes com provisioning
```

## Provisioning
O projeto utiliza shell scripts para provisionamento automático de serviços como Nginx e Apache2.