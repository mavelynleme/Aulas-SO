# RELATÓRIO DE PLANEJAMENTO DE INFRAESTRUTURA
## Estudo de Caso I – Sistemas Operacionais

**Aluno:** ______________________________________  
**Curso:** ______________________________________  
**Disciplina:** Sistemas Operacionais  
**Professor:** Prof. Me. Deivison S. Takatu  
**Data:** ____/____/______

---

## 1. Introdução

A empresa DevStore é uma startup de desenvolvimento de sites que enfrenta desafios relacionados à escalabilidade, organização e segurança de sua infraestrutura de TI. Atualmente, utiliza servidores locais sem padronização, o que dificulta o crescimento e a gestão eficiente dos sistemas.

Este relatório tem como objetivo propor uma arquitetura moderna e eficiente, baseada em conceitos de sistemas operacionais, virtualização, containerização e computação em nuvem.

---

## 2. Problemas Identificados

- Falta de padronização dos servidores  
- Baixa escalabilidade  
- Ausência de ambientes separados (desenvolvimento, teste e produção)  
- Falta de versionamento e testes automatizados  
- Riscos de segurança  

---

## 3. Objetivos da Solução

- Melhorar a organização da infraestrutura  
- Garantir escalabilidade  
- Aumentar a segurança dos sistemas  
- Padronizar ambientes de desenvolvimento  
- Reduzir custos com infraestrutura física  

---

## 4. Arquitetura Proposta

A solução proposta é baseada em quatro pilares principais:

### 4.1 Virtualização

A virtualização será utilizada para criar ambientes isolados, principalmente para testes.

**Vantagens:**
- Isolamento entre sistemas  
- Maior segurança  

**Desvantagens:**
- Maior consumo de recursos  

---

### 4.2 Containerização (Docker)

A containerização será utilizada como principal estratégia para execução das aplicações.

**Vantagens:**
- Leveza e rapidez  
- Padronização dos ambientes  
- Facilidade de deploy  
- Portabilidade  

---

### 4.3 Computação em Nuvem

Será utilizada uma plataforma de nuvem para hospedar as aplicações.

**Benefícios:**
- Alta disponibilidade  
- Escalabilidade sob demanda  
- Redução de custos com hardware  

---

### 4.4 Segurança

Serão implementadas as seguintes medidas:

- Controle de acesso por usuários  
- Definição de permissões  
- Uso de firewall  
- Monitoramento contínuo  

---

## 5. Diagrama da Arquitetura

![Diagrama de Arquitetura](diagrama.png)

---

## 6. Descrição do Diagrama

O diagrama representa a arquitetura de infraestrutura proposta para a empresa DevStore, organizada em três camadas principais: **Desenvolvimento, Ambientes de Testes e Infraestrutura em Nuvem**, além de uma camada inferior de **Controle e Gestão Centralizada**.

Na camada de **Desenvolvimento**, os programadores utilizam containers, garantindo padronização e consistência no ambiente de criação das aplicações.

Na camada de **Testes**, são utilizados dois tipos de ambientes: máquinas virtuais (VMs), que oferecem maior isolamento, e containers com Docker, que proporcionam maior desempenho e leveza. Essa etapa valida as aplicações antes do deploy.

Na camada de **Infraestrutura em Nuvem**, as aplicações são hospedadas em serviços como AWS ou Azure, garantindo alta disponibilidade e escalabilidade. Também são aplicados mecanismos de segurança, monitoramento e gerenciamento de rede e armazenamento.

O fluxo entre as camadas é representado por setas que indicam o caminho da aplicação desde o desenvolvimento até a produção.

Por fim, a camada de **Controle e Gestão Centralizada** inclui controle de acesso, automação e análise de desempenho, garantindo o funcionamento eficiente do sistema.

---

## 7. Papel dos Sistemas Operacionais

### Desenvolvimento
O sistema operacional gerencia os recursos da máquina do desenvolvedor e executa ferramentas como Docker, permitindo a criação de containers.

### Testes
Nas máquinas virtuais, cada ambiente possui seu próprio sistema operacional completo. Já nos containers, o sistema operacional hospedeiro fornece o kernel necessário para execução.

### Produção (Nuvem)
O sistema operacional gerencia os servidores na nuvem, controlando recursos, segurança e execução das aplicações.

### Controle e Gestão
O sistema operacional atua no controle de usuários, permissões, monitoramento e automação.

---

## 8. Fluxo de Trabalho Proposto

1. Desenvolvimento em ambiente local com containers  
2. Testes em ambientes isolados (containers ou máquinas virtuais)  
3. Integração contínua (CI/CD)  
4. Deploy em ambiente de produção na nuvem  
5. Monitoramento contínuo dos serviços  

---

## 9. Monitoramento e Gerenciamento

O sistema será monitorado constantemente para garantir estabilidade e desempenho.

**Serão analisados:**
- Uso de CPU  
- Uso de memória  
- Armazenamento  
- Disponibilidade dos serviços  

---

## 10. Infraestrutura de Rede e Armazenamento

- Configuração de redes virtuais na nuvem  
- Armazenamento escalável  
- Controle de acesso aos recursos  

---

## 11. Justificativa das Escolhas Técnicas

A escolha por containerização e computação em nuvem se deve a:

- Melhor desempenho  
- Menor custo  
- Alta escalabilidade  
- Facilidade de manutenção  
- Compatibilidade entre sistemas  

---

## 12. Estratégia de Implantação

- Migração gradual dos sistemas locais para a nuvem  
- Criação de ambientes padronizados com Docker  
- Implementação de testes automatizados  
- Configuração de monitoramento  

---

## 13. Estratégia de Manutenção e Expansão

- Atualizações contínuas dos sistemas  
- Monitoramento preventivo  
- Escalabilidade conforme demanda  
- Backup periódico dos dados  

---

## 14. Conclusão

A proposta apresentada resolve os principais problemas da DevStore ao introduzir uma infraestrutura moderna, escalável e segura. A utilização de containers, virtualização e computação em nuvem permite maior eficiência operacional e prepara a empresa para crescimento futuro.

---

## 15. Referências

- TANENBAUM, Andrew S. Sistemas Operacionais Modernos  
- Documentação Docker  
- Documentação AWS  