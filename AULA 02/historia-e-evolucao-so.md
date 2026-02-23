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

# Conclusão

A evolução dos sistemas operacionais acompanha diretamente o desenvolvimento da computação ao longo das décadas. Desde os primeiros computadores baseados em válvulas, que exigiam operação manual e programação direta em linguagem de máquina, até os dispositivos móveis modernos, os sistemas operacionais tornaram-se cada vez mais sofisticados, eficientes e essenciais para o funcionamento dos sistemas computacionais.

## Primeira geração

Na primeira geração, não existiam sistemas operacionais formais.

- O uso dos computadores era totalmente manual, limitado e altamente especializado.  
- Cada programa precisava ser preparado individualmente.  
- Não havia automação no gerenciamento de recursos.  

Essa fase evidenciou a necessidade de mecanismos que facilitassem a execução de programas e reduzissem o trabalho humano repetitivo.

## Segunda geração

Na segunda geração, com a introdução dos **transistores**, surgiram os primeiros **sistemas em lote (batch)**.

- Automatizaram a execução sequencial de programas  
- Reduziram o tempo ocioso das máquinas  
- Aumentaram a eficiência operacional  

Embora ainda não houvesse interação direta com o usuário, essa geração marcou o nascimento dos sistemas operacionais como software responsável por organizar a execução de tarefas.

## Terceira geração

A terceira geração representou um grande salto tecnológico e conceitual.

- Computadores tornaram-se mais poderosos e acessíveis  
- Surgiram **multiprogramação** e **tempo compartilhado**  
- Permitiu execução simultânea de múltiplos programas  
- Possibilitou acesso interativo por vários usuários  

Nesse período, consolidaram-se conceitos essenciais:

- processos  
- escalonamento  
- proteção de memória  
- gerenciamento de recursos  

Todos ainda presentes nos sistemas modernos.

## Quarta geração

Na quarta geração, a popularização dos **microprocessadores** levou ao surgimento dos computadores pessoais.

- A computação saiu dos grandes centros acadêmicos e corporativos  
- Passou a fazer parte do cotidiano das pessoas  

Sistemas como:

- **MS-DOS**  
- **UNIX**  
- **Windows**  
- **Macintosh**

trouxeram diferentes abordagens para interação com o usuário.

As **interfaces gráficas** tornaram o uso do computador mais intuitivo e acessível, ampliando enormemente o público da informática.

Além disso, o crescimento das redes introduziu novos desafios:

- comunicação remota  
- compartilhamento de arquivos  
- sistemas distribuídos  

## Quinta geração

Na quinta geração, os **dispositivos móveis** transformaram novamente o cenário da computação.

- Smartphones e tablets exigiram sistemas otimizados para mobilidade  
- Maior eficiência energética  
- Conectividade constante  
- Interfaces sensíveis ao toque  

Sistemas como:

- **Android**  
- **iOS**

mostram como os sistemas operacionais continuam evoluindo para atender novas demandas tecnológicas e sociais.

Hoje, os sistemas operacionais não apenas gerenciam hardware, mas também oferecem:

- ecossistemas completos de aplicativos  
- serviços em nuvem  
- segurança integrada  
- atualizações contínuas  

## Funções centrais dos sistemas operacionais

De forma geral, observa-se que os sistemas operacionais evoluíram de simples controladores de execução para plataformas complexas responsáveis por:

- Gerenciar recursos de hardware de forma eficiente  
- Fornecer abstrações que simplificam o desenvolvimento de software  
- Permitir execução simultânea de múltiplos processos  
- Garantir segurança e isolamento entre programas  
- Oferecer interfaces amigáveis aos usuários  
- Possibilitar comunicação em rede e computação distribuída  

## Importância atual

Essa evolução demonstra que os sistemas operacionais são elementos centrais na computação moderna.

Eles não apenas tornam o hardware utilizável, mas também definem a forma como usuários e aplicações interagem com os sistemas digitais.

## Tendências futuras

Com o avanço contínuo da tecnologia, novas tendências devem influenciar ainda mais o desenvolvimento dos sistemas operacionais, como:

- computação em nuvem  
- inteligência artificial integrada ao sistema  
- virtualização avançada  
- internet das coisas  
- dispositivos vestíveis  

Cada uma dessas áreas traz novos desafios relacionados a:

- desempenho  
- segurança  
- escalabilidade  
- usabilidade  

## Encerramento

Portanto, compreender a história dos sistemas operacionais é fundamental para entender a computação atual.

O estudo dessa evolução revela como soluções criadas no passado estabeleceram as bases para tecnologias presentes e futuras. Além disso, evidencia que os sistemas operacionais continuarão sendo peças-chave no desenvolvimento tecnológico, adaptando-se constantemente às necessidades dos usuários e às inovações do hardware.

Assim, conclui-se que os sistemas operacionais não são apenas softwares auxiliares, mas sim a **estrutura fundamental que sustenta toda a experiência computacional moderna**, desde grandes servidores corporativos até dispositivos móveis pessoais.
O estudo dessa evolução permite compreender por que os sistemas atuais funcionam da forma que funcionam.

