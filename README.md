# Login.feature
#language: pt

Funcionalidade: Tela de login
Como cliente da EBAC SHOP 
Quero configurar o produto de acordo com meu tamanho e gosto, escolher a quantidade e inserir no carrinho
Logar para vizualizar meus pedidos 
Finalizar o cadastro para concluir a compra 
 

Contexto:
Dado que eu acesse a página da EBAC SHOP

Cenario: Configurar produto
Quando eu escolher o produto e selecionar a cor, tamanho e quantidade máxima de 10 produtos
E inserir no carrinho
Então o carrinho deve mostrar o meu produto 
Se eu limpar deve voltar ao estado original 

Cenário: Login na plataforma 
Quando eu inserir o usuário "saramariags@ebac.com"
E senha "Eb@cshop3"
Então o usuário deve ser direcionado a tela de Checkout
Se o usuário ou senha for digitado errado deve exibir a mensagem "usuário ou senha inválidas"

Cenário: Tela de Checkout
Quando eu clicar em criar cadastrar 
E preencer todos os campos obrigatórios com dados válidos 
Então deve exibir a mensagem "usuário cadastrado com sucesso"
Se email inválido deve exibir mensagem "Email inválido"
Se o cadastro for concluído faltando o preenchimento de algum campo exibir a mensagem "Não houve o preenchimento de todos os campos obrigatórios"

Esquema do Cenário: Cadastro de usuário 
Quando eu digitar o <usuario> 
E a <senha> 
Então devo ser direcionada a tela de <Checkout>

Exemplos: 
usuario | senha | Checkout
Exercícios da Ebac do curso de Qualidade de Software
