# 📦 Repositório de Playbooks Ansible para Máquinas Linux

### Este repositório contém *playbooks* escritos em [Ansible](https://www.ansible.com/) com o objetivo de automatizar tarefas como instalações de ferramentas e verificações básicas de funcionamento em máquinas Linux hospedadas na Google Cloud Platform e AWS.

📌 **Foco principal: Cibersegurança**  
Os playbooks deste repositório estão sendo desenvolvidos com foco em hardening de servidores, análise de vulnerabilidades, auditorias e automação de práticas seguras em ambientes Linux.

---

## 🤖 O que é Ansible?

[Ansible](https://docs.ansible.com/) é uma ferramenta de automação de TI poderosa, usada para configurar sistemas, implantar aplicações e orquestrar tarefas complexas. Ele utiliza arquivos YAML chamados *playbooks* para descrever os estados desejados de uma infraestrutura.

---

## 📁 Playbooks disponíveis

### ✅ `install-k3s.yaml` — Instalação automatizada do K3s

Este playbook realiza a instalação do [K3s](https://k3s.io/), uma versão leve do Kubernetes, em servidores Linux.

**O que ele faz:**
- Instala pacotes básicos (como `curl`, `wget` e `ca-certificates`);
- Baixa e executa o script oficial de instalação do K3s;
- Aguarda a inicialização do cluster (porta 6443);
- Verifica se o serviço do K3s está ativo;
- Exibe a versão instalada do K3s;
- Lista os nós que fazem parte do cluster.

---

### 🧪 `cria-arquivo.yaml` — Teste de execução no AWX

Este playbook serve para testar se o ambiente Ansible AWX está configurado corretamente.

**O que ele faz:**
- Cria um arquivo `/tmp/teste-awx-funcionou.txt` com informações como:
  - Data e hora da execução;
  - Nome e IP do servidor;
  - Usuário e sistema operacional.
- Verifica se o arquivo foi criado com sucesso;
- Exibe o conteúdo inicial do arquivo para confirmação.

Esse teste é útil para validar:
- Conectividade via IAP (caso esteja em uso);
- Acesso SSH;
- Funcionamento do Ansible/AWX no ambiente alvo.

---

## 🚧 Em desenvolvimento...

Outros playbooks estão sendo criados e serão adicionados em breve. 
---
