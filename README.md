# 🖥️ Lab de Infraestrutura Linux (`servidor-infra-linux`)

Este repositório contém a documentação prática e o diário de bordo do meu laboratório de infraestrutura doméstico. O objetivo é registrar as configurações de redes, administração e segurança feitas em um servidor físico antigo utilizando o Ubuntu Server (ambiente CLI).

---

# 🏗️ Hardware e Sistema
*   **Sistema Operacional:** Ubuntu Server (Sem interface gráfica)
*   **Ambiente:** Máquina antiga dedicada conectada via Wi-Fi (configurada via CLI) à rede local


---

## 🔒 Segurança Aplicada (Hardening)

### 1. Chaves Criptografadas no SSH
*   **O que foi feito:** Login por senhas comuns desativado no arquivo `/etc/ssh/sshd_config`. O acesso remoto agora exige obrigatoriamente um par de chaves digitais criptografadas.

### 2. Firewall Ativo (UFW)
*   **O que foi feito:** Configuração de bloqueio total por padrão (`Default Deny`). Apenas o tráfego das seguintes portas foi liberado:
    *   Porta `22/tcp` (Acesso administrativo SSH)
    *   Porta `25565/tcp` (Testes de serviços de rede e jogos)

---

## 🗺️ Próximas Etapas (Roadmap)
- [x] Trocar senhas por chaves digitais no SSH
- [x] Ativar e restringir portas com o Firewall UFW
- [ ] Instalar o Fail2Ban para bloquear IPs suspeitos automaticamente
- [ ] Configurar um servidor DNS local leve (Pi-hole)
