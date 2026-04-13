# 🚀 RELATÓRIO DE PLANEJAMENTO DE INFRAESTRUTURA  
## 🖥️ Estudo de Caso I – Sistemas Operacionais  

---

👤 **Aluno:** Mavelyn Leme, Mauro Jose, Beatriz Proença e Macelle Goes
📚 **Disciplina:** Sistemas Operacionais  
👨‍🏫 **Professor:** Prof. Me. Deivison S. Takatu  
---

## 📌 1. Introdução

A empresa **DevStore** é uma startup de desenvolvimento de sites que enfrenta desafios relacionados à escalabilidade, organização e segurança de sua infraestrutura de TI. Atualmente, utiliza servidores locais sem padronização, dificultando o crescimento e a gestão eficiente dos sistemas.

Este relatório propõe uma arquitetura moderna e eficiente, baseada em conceitos de:

- 🖥️ Sistemas Operacionais  
- 📦 Containerização  
- 🧪 Virtualização  
- ☁️ Computação em Nuvem  

---

## ⚠️ 2. Problemas Identificados

- ❌ Falta de padronização dos servidores  
- 📉 Baixa escalabilidade  
- 🔀 Ausência de ambientes separados  
- 🧪 Falta de testes automatizados  
- 🔓 Riscos de segurança  

---

## 🎯 3. Objetivos da Solução

- ✔️ Melhorar a organização da infraestrutura  
- 📈 Garantir escalabilidade  
- 🔐 Aumentar a segurança  
- 📦 Padronizar ambientes  
- 💰 Reduzir custos  

---

## 🏗️ 4. Arquitetura Proposta

A solução é baseada em quatro pilares:

### 🖥️ 4.1 Virtualização

- 🔒 Isolamento entre sistemas  
- 🛡️ Mais segurança  
- ⚠️ Maior consumo de recursos  

---

### 📦 4.2 Containerização (Docker)

- ⚡ Alta performance  
- 🔁 Portabilidade  
- 🧩 Padronização  
- 🚀 Deploy rápido  

---

### ☁️ 4.3 Computação em Nuvem

- 🌍 Alta disponibilidade  
- 📊 Escalabilidade sob demanda  
- 💸 Redução de custos  

---

### 🔐 4.4 Segurança

- 👤 Controle de acesso  
- 🔑 Permissões  
- 🔥 Firewall  
- 📡 Monitoramento contínuo  

---

## 🖼️ 5. Diagrama da Arquitetura

![Diagrama de Arquitetura](diagrama.png)

---

## 🧾 6. Descrição do Diagrama

O diagrama apresenta a arquitetura dividida em três camadas principais:

### 💻 Desenvolvimento
- Uso de containers  
- Ambiente padronizado  
- Execução local  

### 🧪 Testes
- 🖥️ Máquinas virtuais (VMs)  
- 🐳 Containers Docker  
- ✔️ Validação das aplicações  

### ☁️ Produção (Nuvem)
- Infraestrutura em cloud (AWS/Azure)  
- 🔐 Segurança  
- 📊 Monitoramento  
- 💾 Rede e armazenamento  

### ⚙️ Controle e Gestão
- 👤 Controle de acesso  
- 🤖 Automação  
- 📈 Análise de desempenho  

---

## 🧠 7. Papel dos Sistemas Operacionais

### 💻 Desenvolvimento
- Gerencia recursos locais  
- Executa Docker  

### 🧪 Testes
- VMs → SO completo  
- Containers → uso do kernel  

### ☁️ Produção
- Gerencia servidores e segurança  
- Controla execução das aplicações  

### ⚙️ Gestão
- Controle de usuários  
- Monitoramento  
- Automação  

---

## 🔄 8. Fluxo de Trabalho

```text
Desenvolvimento → Testes → Produção → Monitoramento
