# Laboratório: Alteração de endereço MAC no Kali Linux

## Objetivo
Realizar um teste em ambiente controlado para entender como funciona a alteração temporária do endereço MAC de uma interface de rede.

## Ambiente
- Sistema: Kali Linux
- Máquina virtual: VirtualBox
- Interface utilizada: eth0

## Ferramentas utilizadas
- iproute2 (comando ip)
- macchanger

## Procedimento

### 1. Verificar interfaces de rede

Comando:

ip link show

Resultado:
Interface identificada: eth0

---

### 2. Desativar interface

Comando:

sudo ip link set dev eth0 down

Objetivo:
Desativar temporariamente a interface para permitir a alteração do MAC.

---

### 3. Alterar endereço MAC

Comando:

sudo macchanger -r eth0

Resultado:
MAC alterado temporariamente.

---

### 4. Verificar alteração

Comando:

macchanger -s eth0

---

### 5. Restaurar MAC original

Comando:

sudo macchanger -p eth0

## Aprendizados

- Administração de interfaces Linux
- Conceito de endereço MAC
- Uso de ferramentas de rede
- Prática em ambiente isolado

## Observação

Este laboratório foi realizado em máquina virtual própria para fins educacionais.
