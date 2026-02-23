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

