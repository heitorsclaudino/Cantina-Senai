# Cantina SENAI 🍔 🍟

### O site se encontra disponível neste [link](https://sistema.cantinasenai.com.br/)

#### Desenvolvedores


[Abner](https://github.com/ClaushSouza) | 
[Álvaro](https://github.com/alvarexx) | 
[Bianca](https://github.com/BiancaMarcondes) |
[Eduarda](https://github.com/dudaribas) |
[Fabíola](https://github.com/fabiola-girotti) | 
[Gabriel](https://github.com/Gctyx) | 
[Giovanna](https://github.com/GiPaiva) | 
[Guilherme Cunha](https://github.com/Guigite) |
[Guilherme Leoni](https://github.com/GuiLeoni) | 
[Gustavo Alves](https://github.com/Decompilationist) |
[Gustavo Lima](https://github.com/gustavol1) |
[Heitor](https://github.com/heitorsclaudino) |
[Henrique Botelho](https://github.com/Henrique-Botelho) | 
[Henrique Lobo](https://github.com/HLN-lobo) | 
[Luiz](https://github.com/LAugustoLeite) | 


#### Linguagens e tecnologias

- ***JSX*** -> linguagem de marcação usada no React.js (Html envolvido por JavaScript)
- ***JavaScript*** -> linguagem de programação utilizada na criação da dinâmica e interatividade das páginas, autenticação e segurança do site e comunicação com o servidor e banco de dados
- ***MySQL*** -> banco de dados utilizado
- ***Node.js*** -> Ferramenta usada para facilitar o a comunicação entre o banco de dados e o site


#### Bibliotecas e Frameworks

- ***React.js***
- ***Tailwind.css***
- ***Vite***

### Estrutura do projeto 

- public/: diretório contendo a imagem logo do projeto, publica e disponível no título do HTML principal do site

- src/: diretório contendo os arquivos essenciais do projeto.

- components/: pasta que contém os componentes disponíveis e reutilizáveis no site

- pages/: pasta que contém as páginas principais da aplicação.

#### Arquivos

- api.jsx: arquivo com as configurações básicas para efetuar requisições na nossa API
- App.jsx: arquivo principal que configura as rotas e estrutura geral do site.
- main.jsx: arquivo responsável por renderizar o App.jsx

### Introdução


#### O que é o projeto Cantina SENAI?

O sistema Cantina SENAI consiste em uma plataforma de gerenciamento de produtos e contas pendentes de usuários da cantina do SENAI Suíço-Brasileiro "Paulo Ernesto Tolle". No site, é possível realizar as [operações básicas de CRUD](https://coodesh.com/blog/dicionario/o-que-e-crud/) com os produtos do [cardápio](https://www.cantinasenai.com.br), contas e compras de cada cliente registrado no sistema.

**O sistema apresenta:**

- login no padrão JWT (Json Web Token) e criptografia de senhas para maior segurança :lock:

- envio de e-mail automaticamente após as operações que afetam cliente e cantina (abertura ou fechamento de contas, por exemplo.) para maior tranparência


**Porque desenvolvemos este site?**

facilitar o gerenciamento e controle da cantina
maior autenticidade e tranparência nas relações cliente-cantina
facilitar a atualização dos preços do cardápio

Ao analisarmos a situação da cantina da escola, percebemos que as anotações em caderno diárias feitas pelos funcionários que registravam as contas em aberto dos clientes poderiam se tornar um problema, a medida que, com o tempo, seria cada vez mais difícil de recuperar contas passadas, o que poderia gerar imprecisão pela omissão de dados no cálculo da conta final dos clientes frequentadores da cantina. Por exemplo, se um cliente escolhesse comprar hoje na cantina, mas pagar somente daqui a dois meses, os funcionários seriam responsáveis por verificar essa conta em aberto, voltando dois meses de anotações e arriscando não encontrar partes da conta pendente. 

Ainda pensando nos problemas físicos das anotações, os preços do cardápio da cantina eram atualizados por etiquetas adesivas, que além de não serem uma solução prática, poluiam o cardápio visualmente. Outro problema encontrado no cardápio foi no possível cenário de atualização de produtos, que poderiam sair ou entrar no cardápio acarretando no desenvolvimento de um novo folheto por completo, novamente uma solução nada ideal.

Pensando nesses problemas, desenvolvemos este site para gerenciar os dados de contas pendentes, clientes e produtos disponíveis no cardápio. O que justifica o destaque para as 3 principais entidades do projeto: 

- ***Contas pendentes ou vendas***

- ******
Prints das páginas e explicação resumida

[Página dos clientes](https://drive.google.com/file/d/1NcAT3upoI7PiirHQmPr8KcO8FFAVzMc-/view?usp=drive_link "Página dos clientes da cantina")
