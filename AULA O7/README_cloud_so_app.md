# Manual da Atividade — Cloud SO App

## Links do Projeto

**Repositório no GitHub:**  
https://github.com/mavelynleme/cloud-so-app

**Aplicação publicada no Render:**  
https://cloud-so-app.onrender.com/

---

## Teste Online no Render

A aplicação está disponível online no seguinte endereço:

https://cloud-so-app.onrender.com/

---

## Imagem do Teste Localhost

> Espaço reservado para inserir a imagem da aplicação rodando localmente.

![Aplicação rodando em localhost](./imagens/localhost-cloud-so-app.png)

---

## 1. Introdução

Este manual documenta o desenvolvimento da atividade prática da disciplina de **Nuvem e Sistemas Operacionais**.

A proposta da atividade foi criar uma aplicação web utilizando **Node.js** e **Express.js**, capaz de exibir informações do sistema operacional por meio do módulo nativo `os` do Node.js.

A aplicação foi testada em ambiente local e posteriormente publicada em ambiente de nuvem utilizando a plataforma **Render**.

O objetivo principal foi comparar a execução local com a execução em nuvem, observando diferenças relacionadas ao sistema operacional, hostname, CPU, memória e tempo de atividade do sistema.

---

## 2. Objetivo da Atividade

O objetivo da atividade foi desenvolver uma aplicação chamada `cloud-so-app`, que exibe informações do sistema operacional, como:

- Nome do host;
- Plataforma do sistema operacional;
- Arquitetura;
- Quantidade de CPUs;
- Modelo da CPU;
- Memória total;
- Memória livre;
- Tempo de atividade do sistema.

Além disso, a atividade também teve como objetivo publicar a aplicação em ambiente de nuvem utilizando o Render e comparar os dados exibidos no ambiente local com os dados exibidos no ambiente cloud.

---

## 3. Tecnologias Utilizadas

As tecnologias utilizadas no projeto foram:

- **Node.js**: ambiente de execução JavaScript no backend;
- **Express.js**: framework utilizado para criação do servidor web;
- **HTML**: estrutura da página exibida ao usuário;
- **CSS**: estilização visual da aplicação;
- **Git**: ferramenta de controle de versão;
- **GitHub**: plataforma utilizada para hospedar o código-fonte;
- **Render**: plataforma utilizada para publicar a aplicação em nuvem;
- **PowerShell**: terminal utilizado para execução dos comandos no Windows.

---

## 4. Instalação das Ferramentas

Para desenvolver e executar o projeto, foram necessárias as seguintes ferramentas:

### 4.1 Node.js

O Node.js foi utilizado para executar a aplicação backend em JavaScript.

Para verificar se o Node.js estava instalado, foi utilizado o comando:

```bash
node -v
```

Também foi verificada a instalação do npm:

```bash
npm -v
```

O `npm` é o gerenciador de pacotes do Node.js, utilizado para instalar as dependências do projeto.

---

### 4.2 Git

O Git foi utilizado para versionar o projeto e enviar os arquivos para o GitHub.

Para verificar se o Git estava instalado, foi utilizado o comando:

```bash
git --version
```

---

### 4.3 Visual Studio Code

O Visual Studio Code foi utilizado como editor de código para criar e editar os arquivos do projeto.

---

### 4.4 Conta no GitHub

Foi utilizada uma conta no GitHub para criar o repositório remoto do projeto e armazenar o código-fonte da aplicação.

---

### 4.5 Conta no Render

Foi utilizada uma conta na plataforma Render para publicar a aplicação em ambiente de nuvem.

---

## 5. Criação do Projeto

O projeto foi criado dentro da pasta da atividade com o nome `cloud-so-app`.

Os comandos utilizados foram:

```bash
mkdir cloud-so-app
cd cloud-so-app
npm init -y
```

O comando `npm init -y` criou automaticamente o arquivo `package.json`, responsável por armazenar as informações do projeto, scripts e dependências.

---

## 6. Instalação das Dependências

A principal dependência utilizada foi o Express.js.

A instalação foi feita com o comando:

```bash
npm install express
```

Após a instalação, o arquivo `package.json` passou a registrar o Express como dependência do projeto.

Também foi configurado o script de inicialização:

```json
"scripts": {
  "start": "node index.js"
}
```

Esse script permite iniciar a aplicação com o comando:

```bash
npm start
```

---

## 7. Estrutura do Projeto

A estrutura final do projeto ficou organizada da seguinte forma:

```txt
cloud-so-app/
├── index.js
├── package.json
├── package-lock.json
├── README.md
└── public/
    └── style.css
```

### Descrição dos arquivos

| Arquivo/Pasta | Descrição |
|---|---|
| `index.js` | Arquivo principal da aplicação Node.js/Express |
| `package.json` | Arquivo de configuração do projeto e dependências |
| `package-lock.json` | Arquivo gerado automaticamente pelo npm |
| `README.md` | Manual e documentação da atividade |
| `public/style.css` | Arquivo de estilização da página web |

---

## 8. Desenvolvimento da Aplicação

A aplicação foi desenvolvida utilizando Node.js, Express.js e o módulo nativo `os`.

O módulo `os` permite acessar informações do sistema operacional onde a aplicação está sendo executada.

No projeto, foram utilizadas funções como:

```js
os.hostname()
os.platform()
os.arch()
os.cpus()
os.totalmem()
os.freemem()
os.uptime()
```

Essas funções permitem obter informações como nome do host, plataforma, arquitetura, processador, memória e tempo de atividade do sistema.

---

## 9. Funcionamento da Aplicação

A aplicação cria um servidor web utilizando o Express.js.

Quando o usuário acessa a rota principal `/`, o servidor coleta as informações do sistema operacional e renderiza uma página HTML contendo uma tabela com os dados coletados.

A aplicação utiliza a seguinte configuração de porta:

```js
const PORT = process.env.PORT || 3000;
```

Essa configuração é importante porque:

- Em ambiente local, a aplicação roda na porta `3000`;
- No Render, a porta pode ser definida automaticamente pela variável de ambiente `PORT`.

---

## 10. Execução Local

Para executar a aplicação localmente, foi utilizado o terminal PowerShell dentro da pasta do projeto:

```bash
cd "C:\Users\Work\Desktop\AULA 07\cloud-so-app"
```

Em seguida, as dependências foram instaladas:

```bash
npm install
```

Depois, a aplicação foi iniciada:

```bash
npm start
```

O terminal exibiu a seguinte mensagem:

```txt
Server running on port 3000
```

Com isso, a aplicação pôde ser acessada no navegador pelo endereço:

```txt
http://localhost:3000
```

---

## 11. Resultado do Teste Local

Durante o teste local, a aplicação exibiu as informações do sistema operacional da máquina utilizada.

Resultado observado no ambiente local:

| Informação | Valor Local |
|---|---|
| Hostname | DESKTOP-S13NEU4 |
| Platform | win32 |
| Architecture | x64 |
| Number of CPUs | 4 |
| CPU model | Intel(R) Core(TM) i7-4500U CPU @ 1.80GHz |
| Total memory | 15.88 GB |
| Free memory | 7.20 GB |
| System uptime | 422h 15min 42s |

Esses dados representam a máquina local onde a aplicação foi executada.

---

## 12. Versionamento com Git

Após a criação e teste da aplicação, o projeto foi versionado utilizando Git.

Os comandos utilizados foram:

```bash
git init
git add .
git commit -m "Initial cloud-so-app implementation"
git branch -M main
```

Depois, o repositório remoto foi configurado:

```bash
git remote add origin https://github.com/mavelynleme/cloud-so-app.git
```

Em seguida, o projeto foi enviado para o GitHub:

```bash
git push -u origin main
```

Também foi realizada uma personalização visual da página, adicionando o nome **Mavelyn** e uma identidade visual em tons de rosa.

Após essa alteração, foi feito um novo commit:

```bash
git add .
git commit -m "Personalize UI with Mavelyn branding and pink theme"
git push
```

---

## 13. Publicação no GitHub

O projeto foi publicado no GitHub no seguinte repositório:

https://github.com/mavelynleme/cloud-so-app

O GitHub foi utilizado para armazenar o código-fonte e permitir a integração com o Render.

---

## 14. Publicação no Render

Após o envio do projeto para o GitHub, a aplicação foi publicada na plataforma Render.

O procedimento realizado foi:

1. Acessar o painel do Render;
2. Clicar em **New**;
3. Selecionar **Web Service**;
4. Conectar a conta do GitHub;
5. Escolher o repositório `mavelynleme/cloud-so-app`;
6. Configurar o serviço como aplicação Node.js;
7. Definir os comandos de build e inicialização;
8. Criar o serviço e aguardar o deploy.

---

## 15. Configurações Utilizadas no Render

As configurações utilizadas no Render foram:

| Campo | Valor |
|---|---|
| Source Code | `mavelynleme/cloud-so-app` |
| Name | `cloud-so-app` |
| Language | `Node` |
| Branch | `main` |
| Region | Oregon |
| Build Command | `npm install` |
| Start Command | `node index.js` |
| Instance Type | Free |

A aplicação foi publicada online no endereço:

https://cloud-so-app.onrender.com/

---

## 16. Resultado do Teste no Render

Após o deploy, a aplicação foi acessada pelo navegador por meio do link:

```txt
https://cloud-so-app.onrender.com/
```

No ambiente Render, a aplicação exibiu informações do servidor/container em nuvem, e não da máquina local.

Resultado observado no Render:

| Informação | Valor no Render |
|---|---|
| Hostname | srv-d7rvguvavr4c73a5a29g-hibernate-7cf54ddf7c-mnvwf |
| Platform | PREENCHER |
| Architecture | PREENCHER |
| Number of CPUs | PREENCHER |
| CPU model | PREENCHER |
| Total memory | PREENCHER |
| Free memory | PREENCHER |
| System uptime | PREENCHER |

> Observação: preencha os campos marcados como `PREENCHER` com os valores exibidos na página online do Render.

---

## 17. Comparação entre Ambiente Local e Ambiente em Nuvem

A comparação entre os ambientes permite observar que o mesmo código apresenta informações diferentes dependendo do local onde está sendo executado.

| Informação | Ambiente Local | Ambiente Render | Observação |
|---|---|---|---|
| Hostname | DESKTOP-S13NEU4 | srv-d7rvguvavr4c73a5a29g-hibernate-7cf54ddf7c-mnvwf | No ambiente local, o hostname representa o computador pessoal. No Render, representa o identificador interno do container/servidor em nuvem. |
| Platform | win32 | PREENCHER | Localmente a aplicação rodou em Windows. No Render, normalmente roda em Linux. |
| Architecture | x64 | PREENCHER | A arquitetura pode ser semelhante, mas pertence a hardwares/ambientes diferentes. |
| Number of CPUs | 4 | PREENCHER | A quantidade de CPUs disponíveis depende do ambiente de execução. |
| CPU model | Intel(R) Core(TM) i7-4500U CPU @ 1.80GHz | PREENCHER | Localmente foi utilizado o processador físico da máquina. Na nuvem, o processador pertence à infraestrutura do provedor. |
| Total memory | 15.88 GB | PREENCHER | A memória total local representa a RAM do computador. No Render, representa a memória disponível para o ambiente cloud. |
| Free memory | 7.20 GB | PREENCHER | A memória livre varia conforme o uso do sistema em cada ambiente. |
| System uptime | 422h 15min 42s | PREENCHER | Localmente representa o tempo de atividade do sistema. No Render, representa o tempo de atividade do ambiente/container. |

---

## 18. Análise das Diferenças entre Local e Cloud

Ao executar a aplicação localmente, os dados exibidos pertencem ao computador utilizado pelo aluno. Por isso, o hostname aparece como `DESKTOP-S13NEU4`, a plataforma aparece como `win32`, e os dados de CPU e memória correspondem ao hardware físico da máquina local.

No Render, a aplicação é executada em um ambiente remoto de nuvem. Por esse motivo, o hostname exibido é diferente, representando o identificador interno do container ou servidor utilizado pela plataforma.

O hostname do Render apresentou o seguinte valor:

```txt
srv-d7rvguvavr4c73a5a29g-hibernate-7cf54ddf7c-mnvwf
```

Esse nome indica que a aplicação está rodando em um ambiente controlado pelo provedor de nuvem. A presença do termo `hibernate` está relacionada ao comportamento do plano gratuito do Render, que pode colocar aplicações em hibernação após determinado período sem acesso e reativá-las quando são acessadas novamente.

Essa diferença demonstra que a mesma aplicação pode ser executada em ambientes distintos, utilizando recursos diferentes de sistema operacional, CPU, memória e infraestrutura.

---

## 19. Relação com Conceitos de Sistemas Operacionais

A atividade permite relacionar a aplicação prática com diversos conceitos estudados em Sistemas Operacionais.

---

### 19.1 Processos

Quando a aplicação é iniciada com o comando:

```bash
npm start
```

o sistema operacional cria um processo para executar o Node.js.

Esse processo fica responsável por manter o servidor Express ativo e responder às requisições feitas pelo navegador.

No ambiente local, esse processo é criado no sistema operacional Windows.  
No Render, esse processo é criado em um ambiente de nuvem, normalmente baseado em Linux e executado dentro de infraestrutura gerenciada.

---

### 19.2 Gerenciamento de Memória

A aplicação utiliza as funções:

```js
os.totalmem()
os.freemem()
```

Essas funções permitem visualizar a quantidade total de memória e a memória livre disponível no sistema.

Isso se relaciona diretamente ao gerenciamento de memória feito pelo sistema operacional, que controla a alocação e liberação de memória entre processos e serviços em execução.

---

### 19.3 Uso de CPU

A função:

```js
os.cpus()
```

foi utilizada para obter informações sobre os processadores disponíveis no ambiente de execução.

Com isso, a aplicação exibe a quantidade de CPUs e o modelo do processador.

Esse recurso demonstra como o sistema operacional gerencia e disponibiliza informações sobre os recursos de processamento.

---

### 19.4 Sistema Operacional Hospedeiro

O sistema operacional hospedeiro é o ambiente onde a aplicação está sendo executada.

No teste local, o sistema hospedeiro foi a máquina Windows do aluno.

No Render, o sistema hospedeiro é um ambiente remoto de nuvem, gerenciado pela própria plataforma.

Essa diferença mostra que uma aplicação pode funcionar em diferentes sistemas operacionais, desde que suas dependências sejam compatíveis.

---

### 19.5 Virtualização

A computação em nuvem utiliza virtualização ou conteinerização para executar aplicações em ambientes isolados.

No Render, a aplicação não roda diretamente em uma máquina física dedicada ao aluno. Ela é executada em um ambiente controlado, isolado e gerenciado pelo provedor.

Isso permite que múltiplas aplicações compartilhem a mesma infraestrutura física, mantendo separação lógica entre elas.

---

### 19.6 Computação em Nuvem

A publicação no Render representa o uso de computação em nuvem.

A aplicação deixou de estar disponível apenas no computador local e passou a ser acessível pela internet por meio de uma URL pública:

```txt
https://cloud-so-app.onrender.com/
```

Isso demonstra características importantes da nuvem, como:

- Acesso remoto;
- Publicação de aplicações pela internet;
- Uso de infraestrutura de terceiros;
- Escalabilidade;
- Facilidade de deploy;
- Redução da necessidade de manter servidor físico próprio.

---

## 20. Testes Realizados

Foram realizados os seguintes testes:

### 20.1 Teste Local

O teste local foi realizado acessando:

```txt
http://localhost:3000
```

Resultado:

- A aplicação iniciou corretamente;
- A página foi carregada no navegador;
- As informações do sistema operacional local foram exibidas;
- O nome da autora apareceu na página;
- O tema visual em rosa foi aplicado corretamente.

---

### 20.2 Teste no GitHub

O teste no GitHub consistiu em verificar se os arquivos foram enviados corretamente para o repositório remoto.

Foram verificados os seguintes arquivos:

```txt
index.js
package.json
package-lock.json
README.md
public/style.css
```

Resultado:

- O repositório foi criado corretamente;
- Os arquivos do projeto foram enviados;
- O histórico de commits foi registrado;
- O projeto ficou disponível para integração com o Render.

---

### 20.3 Teste no Render

O teste no Render foi realizado acessando:

```txt
https://cloud-so-app.onrender.com/
```

Resultado:

- O deploy foi realizado com sucesso;
- A aplicação ficou disponível online;
- A página carregou corretamente;
- O nome da autora apareceu na página;
- As informações do ambiente em nuvem foram exibidas;
- Foi possível comparar os dados locais com os dados do Render.

---

## 21. Dificuldades Encontradas

Durante o desenvolvimento da atividade, ocorreram algumas dificuldades relacionadas ao uso do Git e do GitHub.

Uma das dificuldades foi o erro ao executar `npm install` fora da pasta correta do projeto. O erro ocorreu porque o comando foi executado em uma pasta que não continha o arquivo `package.json`.

A solução foi acessar corretamente a pasta do projeto:

```bash
cd "C:\Users\Work\Desktop\AULA 07\cloud-so-app"
```

Depois disso, os comandos funcionaram corretamente:

```bash
npm install
npm start
```

Também houve dificuldade inicial no envio para o GitHub, pois alguns comandos foram digitados juntos na mesma linha. A solução foi executar cada comando separadamente.

Além disso, ocorreu conflito com o repositório remoto, pois o GitHub já possuía um arquivo inicial. Como o projeto local era a versão principal da atividade, foi necessário enviar a versão local para o repositório remoto.

---

## 22. Comandos Principais Utilizados

### Instalação e execução

```bash
npm install
npm start
```

### Git e GitHub

```bash
git init
git add .
git commit -m "Initial cloud-so-app implementation"
git branch -M main
git remote add origin https://github.com/mavelynleme/cloud-so-app.git
git push -u origin main
```

### Atualização após personalização

```bash
git add .
git commit -m "Personalize UI with Mavelyn branding and pink theme"
git push
```

---

## 23. Conclusão

A atividade permitiu compreender de forma prática a relação entre aplicações web, sistemas operacionais e computação em nuvem.

Por meio do desenvolvimento da aplicação `cloud-so-app`, foi possível utilizar o Node.js e o Express.js para criar um servidor web simples, capaz de consultar informações do sistema operacional utilizando o módulo nativo `os`.

Ao executar a aplicação localmente, os dados exibidos corresponderam à máquina pessoal utilizada no desenvolvimento. Já no Render, os dados exibidos corresponderam ao ambiente remoto de nuvem fornecido pela plataforma.

Essa comparação demonstrou que o mesmo código pode ser executado em ambientes diferentes, apresentando informações distintas de hostname, sistema operacional, CPU, memória e tempo de atividade.

Além disso, a atividade permitiu praticar conceitos importantes como processos, gerenciamento de memória, uso de CPU, sistema operacional hospedeiro, virtualização, cloud computing, versionamento com Git, publicação no GitHub e deploy em nuvem com Render.

Portanto, o projeto atingiu o objetivo proposto, demonstrando de forma prática a diferença entre execução local e execução em ambiente cloud.

---

## 24. Identificação

**Projeto:** Cloud SO App  
**Autora:** Mavelyn Leme  
**Disciplina:** Nuvem e Sistemas Operacionais  
**Repositório:** https://github.com/mavelynleme/cloud-so-app  
**Aplicação Online:** https://cloud-so-app.onrender.com/
