# 📘 Resumo AULA 02 Sistemas Operacionais (SO)

## 📚 História dos Sistemas Operacionais

## 📌 Descrição Geral
Este material aborda o **o primeiro capítulo  da história dos sistemas operacionais (TANENBAUM; BOS, 2015)** 
O objetivo é apresentar de forma clara e concisa sobre as principais informações abordadas no livro, relacionados à história e evolução  dos sistemas operacionais.


## 1. Introdução 
Os sistemas operacionais são componentes fundamentais de qualquer sistema computacional moderno. Eles atuam como intermediários entre o hardware e os programas aplicativos, permitindo que usuários e desenvolvedores utilizem o computador de forma eficiente e segura.

Desde os primeiros computadores digitais até os dispositivos móveis atuais, os sistemas operacionais evoluíram significativamente, acompanhando as mudanças na arquitetura de hardware, nas necessidades dos usuários e nas formas de utilização dos computadores.

O estudo da evolução dos sistemas operacionais ajuda a compreender:

- Como surgiram conceitos atuais
- Por que certas técnicas existem
- Quais problemas históricos motivaram soluções modernas
- Como hardware e software evoluem juntos

## 1.1 O que é um sistema operacional?
1.1 O que é um sistema operacional?
Um sistema operacional pode ser definido como o software responsável por controlar o hardware e fornecer serviços para os programas.
Entretanto, essa definição simples não cobre totalmente sua complexidade. Segundo o livro, os sistemas operacionais possuem duas funções principais:

- fornecer abstrações para facilitar o uso do hardware
- gerenciar os recursos do sistema

Essas duas visões são complementares e ajudam a entender o papel do sistema operacional.

## 1.1.1 O sistema operacional como uma máquina estendida

O hardware de um computador é complexo e difícil de programar diretamente.

Dispositivos como:

- discos rígidos  
- memória  
- processadores  
- interfaces de entrada e saída  

possuem características técnicas complicadas e inconsistentes.

Para resolver isso, o sistema operacional cria **abstrações**, que simplificam o uso do hardware.

### Exemplos de abstrações

- arquivos em vez de blocos de disco  
- processos em vez de controle direto da CPU  
- memória virtual em vez de acesso físico direto  

Essas abstrações transformam o hardware “confuso” em uma interface limpa e fácil de usar.

Assim, os programadores podem trabalhar com conceitos simples, sem precisar lidar com detalhes eletrônicos ou físicos.

O sistema operacional, portanto, funciona como uma **máquina estendida**, que apresenta uma versão mais amigável do hardware real.

---

## 1.1.2 O sistema operacional como um gerenciador de recursos

Outra forma de enxergar o sistema operacional é como um **gerenciador de recursos**.

Nesse caso, sua principal função é controlar:

- CPU  
- memória  
- dispositivos de entrada e saída  
- armazenamento  
- rede  

Como vários programas podem rodar simultaneamente, o sistema operacional precisa decidir:

- quem usa qual recurso  
- por quanto tempo  
- quando liberar o recurso  
- como evitar conflitos  

### Multiplexação de recursos

O compartilhamento pode ocorrer de duas formas:

#### Multiplexação no tempo

O recurso é usado por vários programas em momentos diferentes.

**Exemplo:**

- CPU alternando entre vários processos  
- impressora atendendo várias tarefas na fila  

#### Multiplexação no espaço

O recurso é dividido em partes.

**Exemplo:**

- memória dividida entre vários programas  
- disco dividido entre arquivos de usuários  

Essa função garante:

- organização  
- eficiência  
- segurança  
- justiça no uso dos recursos  

---

## 1.2 História dos sistemas operacionais

Os sistemas operacionais evoluíram junto com as gerações de computadores.

Essa divisão não é perfeitamente exata, mas ajuda a organizar a evolução histórica.

Cada geração trouxe:

- novos componentes eletrônicos  
- novos modos de uso  
- novas necessidades  
- novas soluções de software  
![Válvulas](images/Colossus.webp)
## Primeiros computadores digitais

Os primeiros computadores digitais surgiram durante e após a Segunda Guerra Mundial.

Eles utilizavam **válvulas eletrônicas** e eram:

- enormes  
- caros  
- pouco confiáveis  
- lentos pelos padrões atuais  

### Exemplos importantes

- ENIAC  
- Colossus  
- Mark I  

### Características dessa geração

- não existiam sistemas operacionais  
- programação feita em **código de máquina**  
- ou por **conexões físicas de cabos**  
- um único grupo fazia tudo (projetar, programar, operar)  
- computadores executavam apenas **um programa por vez**  

### Principais usos

- cálculos científicos  
- tabelas matemáticas  
- trajetórias balísticas  

### Cartões perfurados

No início dos anos 1950, surgiram os **cartões perfurados**, que permitiam:

- escrever programas previamente  
- carregar dados mais facilmente  
- reduzir o uso de painéis de cabos  

Mesmo assim, ainda não havia sistema operacional real.

---

## 1.2.2 A segunda geração (1955–1965): transistores e sistemas em lote (batch)

A invenção do **transistor** tornou os computadores:

- menores  
- mais rápidos  
- mais confiáveis  

Isso permitiu sua comercialização e uso em:

- universidades  
- governos  
- grandes empresas  

### Separação de funções

Pela primeira vez houve divisão entre:

- projetistas  
- operadores  
- programadores  
- manutenção  

### Problema: desperdício de tempo

O computador ficava ocioso enquanto:

- operadores carregavam cartões  
- compiladores eram preparados  
- saídas eram recolhidas  

### Solução: sistemas em lote (batch)

Nos sistemas **batch**:

- vários programas eram reunidos em um lote  
- os cartões eram convertidos em **fita magnética**  
- o computador executava automaticamente cada tarefa  
- a saída era gravada em outra fita  
- depois impressa separadamente  

Isso reduzia o tempo perdido e aumentava a eficiência.

### Surgimento dos primeiros sistemas operacionais simples

Programas especiais passaram a:

- ler tarefas da fita  
- executá-las em sequência  
- controlar entrada e saída  

Eles foram os **precursores dos sistemas operacionais modernos**.

---

## 1.2.3 A terceira geração (1965–1980): circuitos integrados e multiprogramação

Com os **circuitos integrados (CIs)**, os computadores ficaram ainda mais poderosos.

Um marco importante foi a família **IBM System/360**, que introduziu:

- compatibilidade entre modelos  
- arquitetura padronizada  
- grande variedade de aplicações  

### OS/360

Criado para rodar em todos os modelos da linha.

Era:

- enorme  
- complexo  
- cheio de erros inicialmente  
- mas muito influente  

### Multiprogramação

Grande inovação dessa geração.

Permitia:

- vários programas na memória ao mesmo tempo  
- CPU alternando entre eles  
- evitar tempo ocioso durante operações de E/S  

Isso aumentou drasticamente a eficiência do sistema.

### Spooling

Outra técnica importante:

- tarefas eram carregadas do cartão para o disco  
- o sistema buscava novas tarefas automaticamente  
- eliminava transporte manual de fitas  

### Timesharing (tempo compartilhado)

Sistema interativo em que:

- vários usuários acessam o computador simultaneamente  
- cada um usa um terminal  
- CPU alterna rapidamente entre usuários  

Isso reduziu o tempo de resposta e melhorou a produtividade.

### Exemplos históricos

- **CTSS (MIT)**  

Também surgiu o projeto **MULTICS**, que buscava criar um sistema compartilhado gigante para muitos usuários — conceito que influenciou sistemas posteriores.

## 1.2.4 A quarta geração (1980–presente): computadores pessoais

A quarta geração é marcada pela **popularização dos microprocessadores** e pelo surgimento dos **computadores pessoais (PCs)**.

Diferentemente das gerações anteriores, dominadas por grandes mainframes, essa fase trouxe o computador para:

- escritórios  
- escolas  
- pequenas empresas  
- residências  

Isso transformou profundamente a relação entre pessoas e tecnologia.

### Surgimento do computador pessoal

O desenvolvimento de microprocessadores permitiu construir computadores:

- menores  
- mais baratos  
- acessíveis ao público geral  

Um marco importante foi o lançamento do **IBM PC (1981)**, que ajudou a padronizar o mercado.  
Outro marco relevante foi o **Apple Macintosh**, que popularizou interfaces gráficas.

### Sistemas operacionais dessa geração

No início, os sistemas operacionais para PCs eram simples. Geralmente:

- executavam apenas um programa por vez  
- possuíam pouca proteção de memória  
- tinham interface baseada em texto  

Um exemplo clássico foi o **MS-DOS**, que dominou os PCs da IBM por anos.

Com o aumento do poder de hardware, surgiram sistemas operacionais mais avançados, como:

- Windows  
- macOS  
- Linux  

Esses sistemas passaram a oferecer:

- multitarefa  
- suporte a redes  
- interface gráfica amigável  
- gerenciamento avançado de memória  
- segurança de usuários  

### Interfaces gráficas (GUI)

Uma mudança fundamental foi a adoção das **interfaces gráficas de usuário (GUI)**.

**Antes:**

- comandos digitados manualmente  
- aprendizado mais difícil  
- uso restrito a especialistas  

**Com GUI:**

- uso de mouse  
- janelas  
- ícones  
- menus  

Isso tornou o computador acessível a qualquer pessoa e foi decisivo para a popularização da informática.

### Redes e sistemas distribuídos

Com o crescimento das redes locais e da internet, os sistemas operacionais passaram a incluir:

- protocolos de rede integrados  
- compartilhamento de arquivos  
- suporte a múltiplos usuários conectados  
- comunicação entre computadores  

Surgiram também conceitos como:

- computação cliente-servidor  
- sistemas distribuídos  
- serviços de rede integrados ao sistema operacional  

### Multiprocessamento

Outro avanço foi o suporte a:

- múltiplos processadores  
- múltiplos núcleos  
- paralelismo  

Os sistemas operacionais passaram a gerenciar:

- sincronização de processos  
- escalonamento paralelo  
- uso eficiente de CPU multicore  

Isso permitiu aumento significativo de desempenho.

### Virtualização

A **virtualização** também ganhou força. Ela permite:

- executar vários sistemas operacionais no mesmo hardware  
- isolar ambientes  
- testar softwares com segurança  

Isso se tornou fundamental em:

- servidores  
- computação em nuvem  
- ambientes corporativos  
- desenvolvimento de software  

---

## 1.2.5 A quinta geração (1990–presente): computadores móveis

A quinta geração é caracterizada pela ascensão dos **dispositivos móveis**, incluindo:

- smartphones  
- tablets  
- relógios inteligentes  
- dispositivos embarcados  

Esses equipamentos mudaram novamente o conceito de computação.

Hoje o computador:

- está sempre ligado  
- acompanha o usuário  
- depende de conectividade constante  
- precisa consumir pouca energia  

### Sistemas operacionais móveis

Os sistemas operacionais móveis lidam com novos desafios:

- bateria limitada  
- sensores diversos  
- conectividade sem fio  
- interfaces sensíveis ao toque  
- mobilidade constante  

Principais exemplos:

- Android  
- iOS  

Eles oferecem:

- gerenciamento agressivo de energia  
- suspensão automática de aplicativos  
- segurança por permissões  
- lojas de aplicativos  
- atualização remota  

### Computação ubíqua

A computação deixou de ser centralizada e está presente em:

- carros  
- televisores  
- eletrodomésticos  
- sistemas industriais  
- dispositivos IoT  

Isso exige sistemas operacionais:

- leves  
- especializados  
- seguros  
- confiáveis  

Muitos dispositivos usam versões adaptadas de:

- Linux embarcado  
- RTOS (sistemas de tempo real)  

### Segurança e conectividade

Com a mobilidade, surgiram novas preocupações:

- proteção de dados pessoais  
- criptografia  
- autenticação biométrica  
- controle de permissões  
- atualização automática contra vulnerabilidades  

Os sistemas operacionais modernos precisam equilibrar:

- segurança  
- desempenho  
- consumo de energia  
- experiência do usuário  

---

## Conclusão da evolução histórica

A história dos sistemas operacionais mostra uma evolução contínua:

- computadores sem sistema operacional  
- processamento em lote  
- multiprogramação e timesharing  
- computadores pessoais com GUI  
- dispositivos móveis e computação ubíqua  

Cada etapa surgiu para resolver limitações da anterior.

Hoje, os sistemas operacionais são:

- extremamente complexos  
- altamente otimizados  
- essenciais para qualquer dispositivo computacional  

Eles continuam evoluindo para suportar:

- computação em nuvem  
- inteligência artificial  
- internet das coisas  
- sistemas autônomos  

O estudo dessa evolução permite compreender por que os sistemas atuais funcionam da forma que funcionam.

