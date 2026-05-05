# Relatório Comparativo — Render x Railway

**Projeto:** Dashboard de Monitoramento do Sistema Operacional  
**Disciplina:** Sistemas Operacionais  
**Aplicação analisada:** API/Dashboard Node.js + Express  
**Plataformas comparadas:** Render e Railway  


## Links do projeto

- **Aplicação no Render:** https://dashboard-so-hyrk.onrender.com/
- **Aplicação no Railway:** https://dashboard-so-production.up.railway.app/
- **Repositório GitHub:** https://github.com/mavelynleme/dashboard-so
---

## 1. Objetivo do relatório

Este relatório tem como objetivo comparar a execução da mesma aplicação em duas plataformas de hospedagem em nuvem: **Render** e **Railway**.

A aplicação utilizada para a comparação foi um dashboard desenvolvido com **Node.js** e **Express**, capaz de exibir informações do ambiente de execução, como sistema operacional, memória RAM, CPU, rede, arquivos do projeto, variáveis básicas de ambiente e status da aplicação.

A proposta da comparação é observar como a mesma aplicação se comporta em servidores diferentes, analisando características do ambiente, facilidade de deploy, configuração, recursos disponíveis e diferenças percebidas durante a execução.

---

## 2. Tecnologias utilizadas no projeto

- **Node.js:** ambiente de execução JavaScript no servidor.
- **Express:** framework utilizado para criar o servidor web e as rotas da aplicação.
- **HTML, CSS e JavaScript:** utilizados para construir a interface visual do dashboard.
- **Módulo `os` do Node.js:** utilizado para coletar informações do sistema operacional.
- **Módulo `fs` do Node.js:** utilizado para listar arquivos do projeto.
- **Render:** primeira plataforma de hospedagem em nuvem analisada.
- **Railway:** segunda plataforma de hospedagem em nuvem analisada.
- **GitHub:** utilizado como repositório do projeto e base para deploy.

---

## 3. Ambientes analisados

### 3.1 Render

No Render, a aplicação foi executada como um serviço web Node.js. O dashboard identificou o ambiente como **Render / Nuvem**.

Principais informações observadas no dashboard hospedado no Render:

| Item | Valor observado |
|---|---|
| Plataforma detectada | Render / Nuvem |
| Sistema operacional | Linux |
| Usuário do sistema | `render` |
| Diretório home | `/opt/render` |
| Porta utilizada | `10000` |
| NODE_ENV | `production` |
| IP principal | `10.26.92.236` |
| Memória RAM total | Aproximadamente `30.65 GB` |
| Memória RAM em uso | Aproximadamente `20.67 GB` |
| CPU média | Aproximadamente `50%` |
| Núcleos detectados | `8` |
| Modelo de CPU | AMD EPYC 7R13 Processor |
| Kernel/Release | `6.8.0-1050-aws` |
| Node.js | `v25.9.0` |
| Status | Online |

A presença do termo `aws` no kernel indica que a infraestrutura utilizada pelo Render pode estar baseada em ambiente de nuvem sobre AWS ou infraestrutura compatível. O usuário `render`, o diretório `/opt/render` e a porta `10000` também demonstram que a plataforma fornece um ambiente próprio e padronizado para execução da aplicação.

---

### 3.2 Railway

No Railway, a mesma aplicação foi executada também como serviço web Node.js. O dashboard identificou o ambiente como **Railway / Nuvem**.

Principais informações observadas no dashboard hospedado no Railway:

| Item | Valor observado |
|---|---|
| Plataforma detectada | Railway / Nuvem |
| Sistema operacional | Linux |
| Usuário do sistema | `root` |
| Diretório home | `/root` |
| Porta utilizada | `8080` |
| NODE_ENV | `production` |
| IP principal | `10.201.149.239` |
| Memória RAM total | Aproximadamente `371.75 GB` |
| Memória RAM em uso | Aproximadamente `270.16 GB` |
| CPU média | Aproximadamente `15%` |
| Núcleos detectados | `48` |
| Modelo de CPU | Intel Xeon 6975P-C |
| Kernel/Release | `6.18.15+deb13-cloud-amd64` |
| Node.js | `v18.20.8` |
| Status | Online |

No Railway, o ambiente apresentou uma quantidade maior de núcleos de CPU detectados e memória total aparente. Isso não significa necessariamente que toda essa capacidade esteja dedicada exclusivamente à aplicação, pois plataformas em nuvem geralmente utilizam virtualização, containers e compartilhamento de recursos entre serviços.

---

## 4. Comparação direta entre Render e Railway

| Critério | Render | Railway |
|---|---|---|
| Tipo de plataforma | Plataforma de deploy em nuvem para aplicações, APIs e serviços web | Plataforma de deploy em nuvem para aplicações, bancos, serviços e projetos completos |
| Facilidade de deploy | Simples, com conexão ao GitHub e configuração de build/start command | Muito simples, com conexão ao GitHub e deploy rápido |
| Ambiente detectado | Render / Nuvem | Railway / Nuvem |
| Sistema operacional | Linux | Linux |
| Usuário do processo | `render` | `root` |
| Porta usada pela aplicação | `10000` | `8080` |
| Diretório padrão | `/opt/render` | `/app` e `/root` |
| CPU detectada | AMD EPYC 7R13, 8 núcleos | Intel Xeon, 48 núcleos |
| Memória total aparente | Cerca de 30.65 GB | Cerca de 371.75 GB |
| Identificação de nuvem | Kernel com referência a AWS | Kernel cloud amd64 |
| NODE_ENV | production | production |
| Interface da plataforma | Mais guiada e tradicional | Mais moderna e centrada em projetos |
| Indicação para iniciantes | Muito boa | Muito boa |
| Organização de serviços | Serviços separados por tipo | Projeto agrupando serviços, variáveis e recursos |
| Configuração de variáveis | Simples via painel | Simples via painel, com forte integração no projeto |
| Melhor ponto observado | Ambiente previsível e fácil de entender | Deploy rápido e estrutura moderna para múltiplos serviços |

---

## 5. Principais diferenças técnicas observadas

### 5.1 Porta de execução

Uma diferença importante foi a porta utilizada em cada ambiente.

No **Render**, a aplicação utilizou a porta `10000`. Já no **Railway**, a aplicação utilizou a porta `8080`.

Isso demonstra a importância de configurar aplicações Node.js usando:

```js
const PORT = process.env.PORT || 3000;
```

Dessa forma, a aplicação consegue funcionar corretamente tanto localmente quanto em plataformas de nuvem, respeitando a porta definida automaticamente pelo ambiente.

---

### 5.2 Usuário do sistema

No Render, a aplicação foi executada com o usuário:

```text
render
```

No Railway, a aplicação foi executada com o usuário:

```text
root
```

Essa diferença mostra que cada plataforma prepara o container ou ambiente de execução de uma forma diferente. Para aplicações simples, isso normalmente não altera o funcionamento. Porém, em projetos maiores, permissões de arquivos, diretórios temporários e segurança podem ser impactados.

---

### 5.3 Diretórios do ambiente

No Render, o diretório home foi identificado como:

```text
/opt/render
```

No Railway, o ambiente apresentou diretórios como:

```text
/root
/app
```

Essa diferença mostra que os caminhos internos de arquivos variam de acordo com a plataforma. Por isso, uma boa prática é evitar caminhos absolutos fixos no código e utilizar recursos como:

```js
process.cwd()
path.join()
```

---

### 5.4 Recursos de CPU e memória

O Railway apresentou valores maiores de CPU e memória total detectada pelo sistema. O Render apresentou valores menores, mas ainda suficientes para a aplicação analisada.

No entanto, esses dados devem ser interpretados com cuidado. Em ambientes de nuvem, o sistema pode apresentar informações do host, do container ou de uma camada virtualizada. Portanto, a quantidade de CPU e memória exibida pelo dashboard não significa necessariamente que todos esses recursos estejam reservados exclusivamente para a aplicação.

---

### 5.5 Kernel e infraestrutura

No Render, o kernel exibido continha referência a AWS:

```text
6.8.0-1050-aws
```

No Railway, o kernel apareceu como:

```text
6.18.15+deb13-cloud-amd64
```

Isso demonstra que ambas as plataformas utilizam ambientes Linux em nuvem, mas com imagens, kernels e infraestrutura diferentes.

---

## 6. Diferenças entre as ferramentas

### Render

O Render é uma plataforma bastante direta para publicar aplicações web, APIs, bancos de dados, serviços e tarefas agendadas. Uma vantagem observada é a simplicidade do painel e do processo de deploy. Para projetos acadêmicos, APIs pequenas e aplicações Node.js, o Render é fácil de configurar e entender.

Pontos positivos do Render:

- Deploy simples via GitHub.
- Boa organização por serviço.
- HTTPS automático.
- Ambiente fácil de compreender.
- Boa opção para projetos acadêmicos.
- Configuração simples de build e start command.
- Identificação clara de variáveis como `PORT` e `NODE_ENV`.

Pontos de atenção do Render:

- Algumas configurações podem exigir ajuste manual.
- Em planos gratuitos ou básicos, pode haver limitações de recurso.
- Dependendo do plano, aplicações podem ter comportamento de hibernação ou cold start.
- O deploy pode ser um pouco mais demorado em alguns casos.

---

### Railway

O Railway também oferece deploy rápido via GitHub, mas sua organização é mais centrada no conceito de projeto. Ele facilita a criação de serviços, bancos de dados e variáveis de ambiente dentro de um mesmo espaço.

Pontos positivos do Railway:

- Deploy muito rápido.
- Interface moderna.
- Boa organização por projeto.
- Facilidade para adicionar serviços e bancos de dados.
- Gerenciamento prático de variáveis de ambiente.
- Boa experiência para aplicações modernas e microsserviços.

Pontos de atenção do Railway:

- O modelo de uso e cobrança precisa ser acompanhado com atenção.
- A estrutura pode esconder detalhes internos do ambiente.
- Para iniciantes, alguns conceitos de projeto, serviço e ambiente podem exigir adaptação.
- O ambiente pode apresentar recursos aparentes maiores que não necessariamente são dedicados somente à aplicação.

---

## 7. Comparação de uso prático

Durante os testes, as duas plataformas conseguiram executar a mesma aplicação Node.js + Express com sucesso.

A aplicação ficou online nos dois ambientes, respondeu às rotas principais e exibiu informações do sistema operacional. Isso demonstra que tanto Render quanto Railway são adequados para hospedar aplicações web simples e APIs acadêmicas.

Rotas utilizadas na aplicação:

| Rota | Função |
|---|---|
| `/` | Exibe o dashboard visual |
| `/api/system` | Retorna os dados do sistema em JSON |
| `/health` | Retorna o status de saúde da aplicação |

---

## 8. Qual plataforma foi melhor para este projeto?

Para este projeto específico, as duas plataformas atenderam bem ao objetivo.

O **Render** se destacou por ser mais direto, previsível e fácil de explicar em um contexto acadêmico. A separação por serviço, a porta `10000` e o ambiente com usuário `render` deixam claro que a aplicação está rodando em uma plataforma gerenciada.

O **Railway** se destacou pela experiência moderna, pela rapidez no deploy e pela organização do projeto. Ele parece mais flexível para evoluir a aplicação com banco de dados, múltiplos serviços e variáveis de ambiente.

Para uma primeira publicação acadêmica, o Render pode ser considerado mais simples de apresentar. Para evolução futura com mais serviços, banco de dados e arquitetura mais completa, o Railway pode ser uma opção mais prática.

---

## 9. Conclusão

A comparação entre Render e Railway mostrou que ambas as plataformas são eficientes para hospedar aplicações Node.js com Express.

O Render apresentou um ambiente mais simples, direto e previsível, sendo bastante adequado para projetos acadêmicos e APIs pequenas. O Railway apresentou uma estrutura mais moderna e flexível, com foco em projetos compostos por múltiplos serviços.

As diferenças observadas no dashboard, como porta utilizada, usuário do sistema, diretórios internos, quantidade de CPU, memória e kernel, demonstram que cada plataforma utiliza uma infraestrutura própria para executar a aplicação.

A principal conclusão é que aplicações preparadas corretamente para nuvem devem evitar configurações fixas, usar `process.env.PORT`, tratar variáveis de ambiente com segurança e não depender de caminhos absolutos do sistema operacional.

Assim, o projeto atingiu o objetivo de demonstrar, na prática, como uma aplicação Node.js pode ser executada em diferentes ambientes cloud e como cada servidor apresenta características próprias de sistema operacional, rede, CPU, memória e configuração.

---





