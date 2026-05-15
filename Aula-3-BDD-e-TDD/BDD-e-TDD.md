# Anotações

## BDD para rotina CRUD de um sistema web + Login

* Login com campos preenchidos corretamente
Dado que estou na tela de login e preencho os campos corretamente, quando clico no botão entrar então o sistema me informa que o login foi bem sucedido e redireciona para a tela de home da aplicação

* Login com campos faltando
Dado que estou na tela de login e não preencho todos os campos corretamente, quando clico no botão entrar então os sistema destaca os campos faltantes com contorno vermelho e com a mensagem "Preencha {nome do campo}" abaixo do campo. 

* Login com senha incorreta
Dado que estou na tela de login e preencho o campo email corretamente e com campo senha incorreto, quando clico no botão cadastrar então o sistema retorna um modal informando o seguinte erro "Não foi possível realizar o login!"

* Cadastrar usuário com campos preenchidos corretamente
Dado que estou na tela para cadastro de usuário e preencho os campos corretamente, quando clico no botão cadastrar então o sistema cadastra o usuário no banco e me redireciona para a tela de login

* Cadastrar usuário com campos faltando 
Dado que estou an tela para cadastro de usuário e não preencho todos os campos, quando clico no botão cadastrar então o sistema retorna informando o erro "Preencha todos os campos de cadastro!"

* Cadastrar usuário com campos incorretos
Dado que estou na tela para cadastro de usuário e preencho os campos incorretamente, quando clico no botão cadastrar então o sistema retorna um modal informando o seguinte erro "Campo inseridos incorretamente!" e uma lista dos campos inseridos incorretamente.

* Requisitar vários usuários
Dado que preciso verificar os usuários cadastrados, quando entro na tela de usuários cadastrados entãos o sistema retorna os usuários e suas informações em uma lista organizada com formato de tabela.

* Requisitar um usuário pelo ID
Dado que estou na tela de usuários cadastrados e insiro um ID no campo de filtro, quando clico no botão filtrar então os sistema me retorna a lista organizada com formato de tabela com apenas o usuário do ID solicitado.

* Requisitar um usuário com ID não existente
Dado que estou na tela de usuários cadastrados e insiro um ID não cadastrado no campo de filtro, quando clico no botão filtrar então os sistema me retorna uma mensagem de erro dizendo "Usuário não encontrado!".

* Atualizar o cadastro do usuário alterando apenas um campo
Dado que estou na tela de alteração do usuário e altero apenas um dos campos registrados, quando clico no botão alterar então o sistema altera apenas o campo em questão, redireciona para a tela de usuários cadastrados com uma notificação no canto superior direito da tela dizendo "Usuário alterado com sucesso!" e os dados atualizados do usuário.

* Atualizar o cadastro do usuário inserindo um dado inválido no campo
Dado que estou na tela de alteração do usuário e altero um ou mais campos para um formato inválido no campo, quando clico no botão alterar então o sistema destaca os campos que estão com formato incorreto em vermelho e embaixo do campo imprime a mensagem "Dado inválido!"

* Atualizar o cadastro do usuário inserindo dado unico já cadastrado
Dado que estou na tela de alteração do usuário e altero um campo único para um valor já cadastrado no banco, quando clico no botão alterar então o sistema destaca o campo já cadastrado e embaixo do campo imprime a mensagem "Dado inválido!"

* Deletar um usuário existente no banco
Dado que estou na tela de usuários cadastrados, quando clico no botão deletar do registro do usuário e confirmo a remoção então o sistema altera o status do usuário para inativo, deletando-o efetivamente do banco após o prazo de 30 dias e redireciona para a página de usuários.

* Deletar um usuário instantaneamente
Dado que tenho o maior nível de acesso e estou na tela de usuários cadastrados, clico no botão deletar do registro de usuário e marco o campo "Remoção completa" então o sistema deleta o registro do usuário.

* Deletar um usuário com uma sessão em aberto
Dado que estou na tela de usuário cadastrados, quando clico no botão para deletar um usuário com uma sessão ativa então o sistema retorna que não é possível deletar o usuário e mostra a opção para matar as sessões.