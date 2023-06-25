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

- ***JSX*** - linguagem de marcação usada no React.js (Html envolvido por JavaScript)
- ***JavaScript*** - linguagem de programação utilizada na criação da dinâmica e interatividade das páginas, autenticação e segurança do site e comunicação com o servidor e banco de dados
- ***MySQL*** - banco de dados utilizado
- ***Node.js*** - Ferramenta usada para facilitar o a comunicação entre o banco de dados e o site


#### Bibliotecas e Frameworks

- ***React.js*** - uma biblioteca JavaScript utilizada para auxiliar o desenvolvimento das páginas

- ***Tailwind.css*** - uma biblioteca utilizada para facilitar e dinamizar a estilização das páginas

- ***Vite*** - um framework utilizado para simplificar a estrutura do projeto (me corrijam henrique e guilherme, pra ver se é isso mesmo)

### Estrutura do projeto 

#### Pastas

- public/: pasta contendo a imagem logo do projeto, publica e disponível no título do HTML principal do site

- src/: pasta contendo os arquivos essenciais do projeto.

- components/: pasta que contém os componentes disponíveis e reutilizáveis no site

- pages/: pasta que contém as páginas principais da aplicação.

#### Arquivos

- api.jsx: arquivo com as configurações básicas para efetuar requisições na nossa API
- App.jsx: arquivo principal que configura as rotas e estrutura geral do site.
- main.jsx: arquivo responsável por renderizar o App.jsx

## Introdução


#### O que é o projeto Cantina SENAI?

O sistema Cantina SENAI consiste em uma plataforma de gerenciamento de produtos e contas pendentes de usuários da cantina do SENAI Suíço-Brasileiro "Paulo Ernesto Tolle". No site, é possível realizar as [operações básicas de CRUD](https://coodesh.com/blog/dicionario/o-que-e-crud/) com os produtos do [cardápio da cantina do SENAI](https://www.cantinasenai.com.br), contas e compras de cada cliente registrado no sistema.

**O sistema apresenta:**

- login no padrão JWT (Json Web Token) e criptografia de senhas para maior segurança :lock:

- envio de e-mail automaticamente após as operações que afetam cliente e cantina (abertura ou fechamento de contas, por exemplo.) para maior tranparência


**Porque desenvolvemos este site?**


Ao analisarmos a situação da cantina da escola, percebemos que as anotações em caderno diárias feitas pelos funcionários que registravam as contas em aberto dos clientes poderiam se tornar um problema, a medida que, com o tempo, seria cada vez mais difícil de recuperar contas passadas, o que poderia gerar imprecisão pela omissão de dados no cálculo da conta final dos clientes frequentadores da cantina. Por exemplo, se um cliente escolhesse comprar hoje na cantina, mas pagar somente daqui a dois meses, os funcionários seriam responsáveis por verificar essa conta em aberto, voltando dois meses de anotações e arriscando não encontrar partes da conta pendente. 

Ainda pensando nos problemas físicos das anotações, os preços do cardápio da cantina eram atualizados por etiquetas adesivas, que além de não serem uma solução prática, poluiam o cardápio visualmente. Outro problema encontrado no cardápio foi no possível cenário de atualização de produtos, que poderiam sair ou entrar no cardápio acarretando no desenvolvimento de um novo folheto por completo, novamente uma solução nada ideal.

O site ainda possibilita maior transparência nas relações cantina-cliente uma vez que ao registrar uma nova compra pra determindao cliente, envia um e-mail automaticamente com os detalhes da compra (produtos comprados e seu valor) para o respectivo consumidor.

Pensando nesses problemas, desenvolvemos este site para gerenciar os dados de contas pendentes, clientes e produtos disponíveis no cardápio. Por isso, vamos dar destaque para as 3 principais entidades do projeto. Qualquer pessoa com acesso autorizado a aplicação pode realizar as 4 operações de CRUD com: 

- ***Contas pendentes ou vendas*** - Possuem compras onde cada uma tem: um cliente a quem está associada,  produtos comprados, data e hora do seu registro, detalhes e status de pagamento (Pago | Não pago)

- ***Clientes*** - Possuem dados como nome, e-mail e telefone

- ***Produtos disponíveis no cardápio*** - Possuem nome, preço, categoria (salgados, doces, etc.) e descrição

Para cada uma das entidades temos uma página específica do site, que conta também com um manual de usuário. Para facilitar a navegação entre as páginas, um menu está disponível em todas as telas da aplicação.

![Um print da tela com o menu aberto exibindo as páginas de navegação: Vendas, Clientes, Produtos e Manual de Usuário. Contém ainda um botão excluir para logout. De fundo, a página do Manual é exibida, na parte do sumário onde links interativos direcionam o leitor para aquela parte específica do manual.](./src/assets/prints/manualEmenu.png "Print do menu expandido e página do manual de instruções")

Após a tela de login (mostrada abaixo), o usuário se validado, é redirecionado para a ***Página de vendas***.

![Um print da tela de login do sistema. A cor de fundo é azul-marinho, os outros detalhes da página estão em vermelho-vinho. A logo representa uma cantina e está no centro da imagem. Abaixo, aparecem os campos de inserção de informações necessárias para realizar o login (e-mail e senha). Mais abaixo há um botão que realiza a o envio dos dados para validação. E por fim, um link com o título "Esqueci minha senha" que, ao ser clicado, solicita o endereço de e-mail para a recuperação da própria.](./src/assets/prints/loginIMGedit.png "Print do login do sistema")

***legenda***: Tela inicial do sistema. Sem um login registrado, esta é a única página que o usuário terá acesso.


#### Página de Vendas

A página de vendas é responsável por gerenciar as contas pendentes dos clientes. Optamos por usar o nome de vendas para auxiliar os funcionários da cantina, que utilizarão a plataforma todos os dias. 
Consiste na apresentação de todas as contas em aberto registradas. Integrada com uma caixa de busca, permite que o funcionário busque todas as compras de um cliente específico, pagas e não pagas.
Permite ainda o pagamento ou a exclusão de compras específicas, ambas ações irreversíveis. 

![No topo e centralizada se encontra a logo do projeto, em tamanho reduzido e cor branca, sobre um fundo azul-marinho (igual ao da tela de login). À direita, um botão com 3 listras brancas indicando um menu expansivo. Quando clicado, expande o menu. No centro da imagem se encontra a "Tabela de vendas", com dados sobre todas as vendas ( ou compras se olhadas pela ótica dos clientes). Ao lado do título, totalmente a direita, dois botões "Excluir vendas pagas" ( em cor vermelha) e "Adicionar venda" (em cor verde) estão posicionados. Serão explicados logo após a imagem. Logo abaixo do título se encontra uma caixa de pesquisa, que ao ser clicada, possibilita a busca por clientes específicos e seus dados são exibidos. Os dados representados na tabela são: cliente a quem a compra está associada, data e hora da compra, status com as opções "Pago e Não Pago" e valor total da compra. Ainda dentro da tabela, mais à direita, para cada compra, existem 3 botões cujas funcionalidades serão explicadas logo abaixo da imagem. São eles: Pagar (cor verde), Detalhes (cor azul) e Excluir (cor vermelha)](./src/assets/prints/vendasPage.png "Tela de vendas (compras se vistas pelo lado do cliente")
***legenda***: Página de gerenciamento de compras (ou vendas)

A página de vendas exibe os detalhes de todas as vendas (ou compras) registradas no sistema. A estrutura de tabelas adotada foi escolhida para melhor visualização dos dados e será reutilizada por toda a aplicação. 

A seguir, uma breve descrição dos botões e suas funcionalidades:

- ***"Excluir Vendas Pagas"*** - Exclui ***permanentemente*** todas as vendas com status "Pago" do sistema, após confirmação.

- ***"Adicionar venda"*** - Adiciona uma compra a conta de um cliente específico.

- ***"Pagar"*** - Altera o status da compra para "Pago". Após o status alterado, o botão fica desabilitado e na cor cinza. É uma ação permanente.

- ***"Detalhes"*** - Exibe os detalhes da compra (items comprados e seu respectivo valor). 

- ***"Excluir"*** - Exclui ***permanentemente*** a compra do sistema, após confirmação.


Fotos das telas seguintes ou janelas de confirmação dessas operações:

![Uma janela de confirmação aberta ao clicar no botão "Excluir vendas pagas", consiste em um retângulo sobressaltado com o alerta: "Tem certeza que deseja excluir todas as vendas pagas? Essa ação é irreversível". Sua cor é branca e tem dois botões: cancelar (na cor cinza) e sim (na cor azul). Após confirmação, a janela é fechada e a ação completada.](./src/assets/prints/modalExcluiComprasPagas.png.png "Modal de confirmação de exclusão de venda")

![Uma janela com informações sobre a compra. Acionada ao clicar no botão "Detalhes". Consiste em um retângulo sobressaltado com uma tabela exibindo dados como: nome, preço e quantidade dos produtos. Abaixo, o botão "Fechar" é exibido na cor cinza e quando clicado, retorna o usuário para a página de vendas.](./src/assets/prints/detailsCompraEdit.png "Modal detalhes da compra")


![Uma janela de confirmação aberta ao clicar no botão "Excluir". Consiste em um retângulo sobressaltado com o alerta: "Excluir esta venda?". Sua cor é branca e tem dois botões: "Cancelar" (na cor cinza) e "Sim" (na cor azul). Após confirmação, a janela é fechada e a ação completada.](./src/assets/prints/modalExcluiCompra.png.png "Modal de confirmação de exclusão de compra")

***Nota***: nosso sistema não trabalha com transações monetárias, todas suas funcionalidades são para fins de controle e registro. Pagamentos são feitos à parte, diretamente com a cantina.


#### Página de Clientes

A página de clientes é responsável pela adição, edição, exclusão e leitura dos dados dos clientes registrados no sistema. Em um cenário de dados incorretos, por exemplo, ela possibilita fácil atualização.

Além disso, a página possui o botão "Finalizar conta" para cada um dos clientes registrados. Se o cliente tiver uma conta em aberto, o sistema somará todas as suas compras e mostrará o valor total (e individual de cada compra). Ao prosseguir, todas as compras daquele cliente terão seu status alterado para "Pago" e a conta do cliente é fechada.

Se o cliente tiver uma conta fechada, ou seja, sem compras de status "Não pago" registradas, o sistema informará o funcionário e disponibilizará apenas um botão para voltar a tela de clientes.

![No topo e centralizada se encontra a logo do projeto, em tamanho reduzido e cor branca, sobre um fundo azul-marinho (igual ao da tela de login). À direita, um botão com 3 listras indicando um menu expansivo. Quando clicado, expande o menu. No centro da imagem se encontra a "Tabela de Clientes", com dados sobre todas os clientes registrados no sistema. Ao lado do título, totalmente a direita, o botão de cor verde e texto "Adicionar cliente" na cor branca, está posicionado. Novamente, explicações se encontram abaixo da imagem. Abaixo do título se encontra uma caixa de pesquisa, que ao ser clicada, possibilita a busca por clientes específicos e seus dados são exibidos. Os dados representados na tabela são: nome do cliente, telefone celular e e-mail cadastrado. Ainda dentro da tabela, mais à direita, para cada cliente, existem 3 botões cujas funcionalidades serão explicadas logo abaixo da imagem. São eles: Finalizar conta (em azul), Editar (em amarelo) e Excluir (em vermelho).](./src/assets/prints/clientesPage.png "Tela dos clientes")

***legenda***: Página de gerenciamento e visualização de clientes

A página de clientes exibe os detalhes de todos os clientes registrados no sistema. A seguir, uma breve descrição dos botões e suas funcionalidades:

- ***Adicionar cliente*** - carrega uma página que solicita os dados para a criação de um novo cliente.

- ***Editar*** - carrega uma página contendo os dados do cliente a ser alterado e permite qualquer alteração.

- ***Excluir*** - exclui ***permanentemente*** aquele cliente do sistema, após confirmação.

- ***Finalizar conta*** - finaliza a conta em aberto (se houver) somando os totais de todas as compras. Após confirmação, altera o estado de todas as compras para "Pago".

Fotos das telas seguintes ou janelas de confirmação dessas operações:

![Uma janela aberta para inserção dos dados ao clicar no botão "Adicionar cliente". Consiste em um formulário retângular com o título: Novo cliente. Centralizado e destacado sobre um fundo automaticamente ofuscado, sua cor é branca e tem os seguintes campos: nome do cliente e-mail do cliente e telefone do cliente. Abaixo dos campos um botão verde de título "Adicionar" confirma a operação.](./src/assets/prints/modalAddClient.png "Modal adiciona cliente")

![Uma janela nos mesmos padrões visuais da interior. Se difere apenas: no título "Edita cliente", no fato de agora os campos vierem preenchidos com os dados do cliente selecionado e o botão de confirmação tem título "Salvar".](./src/assets/prints/modalEditClient.png "Modal edita cliente")

![Uma janela de confirmação aberta ao clicar no botão "Excluir". Consiste em um retângulo sobressaltado com o alerta: "Excluir cliente?". Sua cor é branca e tem dois botões: "Cancelar" (na cor cinza) e "Sim" (na cor azul). Após confirmação, a janela é fechada e a ação completada.](./src/assets/prints/modalExcluiClient.png "Modal de confirmação exclui cliente")

![Uma janela com informações sobre a compra. Acionada ao clicar no botão "Finalizar conta", consiste em um retângulo sobressaltado com uma tabela exibindo dados como: data e hora, total e um botão levando aos detalhes de cada compra registrada para aquele cliente. Abaixo dos dados, uma linha com o nome "Total:" exibe o total de todas as compras somadas. Por fim, no "pé" da janela o botão "Finalizar conta" é exibido na cor verde e quando clicado, retorna o usuário para a página de clientes, alterando o status de todas as compras daquele cliente para "Pago".](./src/assets/prints/modalFinalizaConta.png "Modal finaliza conta")

#### Página de Produtos

A página de produtos é responsável pela adição, edição, exclusão e leitura dos produtos registrados no sistema e que alimentam o [cardápio da cantina](https://www.cantinasenai.com.br).

![As cores de fundo,o design e a estrutura das outras páginas são preservados. As alterações ocorrem nos dados e botões dispostos na tabela. São representados os dados: nome do produto, categoria (salgados, lanches, doces, etc.), descrição e preço. Acima o botão "Adiciona produto" se encontra, em verde. Para cada produto temos dois botões: Editar (em amarelo) e Excluir (em vermelho).](./src/assets/prints/produtosPageedit.png "Página de produtos")

***legenda***: Tela de gerenciamento e visualização de produtos

A página de produtos exibe os detalhes de todos os produtos registrados no sistema. A seguir, uma breve descrição dos botões e suas funcionalidades:

- ***Adicionar produto*** - carrega uma página que solicita os dados para a criação de um novo produto.

- ***Editar*** - carrega uma página contendo os dados do produto a ser alterado e permite qualquer modificação.

- ***Excluir*** - exclui ***permanentemente*** aquele produto do sistema, após confirmação.

Aqui vão alguns prints das telas de confirmação:

![Uma janela aberta para inserção dos dados ao clicar no botão "Adicionar produto". Consiste em um formulário retângular com o título: Novo produto. Centralizado e destacado sobre um fundo automaticamente ofuscado, sua cor é branca e tem os seguintes campos: nome do produto, preço, categoria e descrição. Abaixo dos campos um botão verde de título "Adicionar" confirma a operação.](./src/assets/prints/modalAddProduto.png "Modal adiciona produto")

![Uma janela nos mesmos padrões visuais da interior. Se difere apenas: no título "Edita produto", no fato de agora os campos vierem preenchidos com os dados do produto selecionado e o botão de confirmação tem título "Salvar".](./src/assets/prints/modalEditProduto.png "Modal edita produto")

![Uma janela de confirmação aberta ao clicar no botão "Excluir". Consiste em um retângulo sobressaltado com o alerta: "Excluir este item?". Sua cor é branca e tem dois botões: "Cancelar" (na cor cinza) e "Sim" (na cor azul). Após confirmação, a janela é fechada e a ação completada.](./src/assets/prints/modalExcluiProduto.png "Modal de confirmação exclui produto")


## Conclusão


O projeto Cantina SENAI foi desenvolvido com muita dedicação e comprometimento, durante um período de aproximadamente 3 meses. Focados em resolver problemas, solucionamos a questão das anotações acrescentando uma interface visualmente agradável, limpa e fluida. O site possui funcionalidades como registro de data e hora de compras, sistema de busca por clientes específicos, envios de e-mail automáticos e etc.

Na parte da segurança, o sistema de login JWT garante que o usuário só acesse a aplicação se devidamente autorizado. Caso contrário, a tentativa de navegação entre outras páginas da aplicação será *barrada* e o usuário redirecionado para a tela de login. O sistema também possui proteção contra *SQL injection* e criptografias de senhas inclusas, para aumentar a segurança contra possíveis invasões.

Todas essas medidas foram implementadas com o objetivo de ***facilitar*** o gerenciamento dos produtos e contas pendentes, promovendo **segurança** e **transparência** na relação cliente-cantina e na ulização de todas as partes da aplicação.

