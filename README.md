# perfil_compras
Exemplo para utilização de identificação de perfil

Neste exemplo:

Criamos três usuários com características distintas (premium, normal e vip), representados pelos perfis dos usuários.
Cada perfil de usuário tem sua própria lista de produtos associada a ele.

Nestas páginas:
________________________________________________________________________________________________________________________
pagina_produtos.html exibe os produtos correspondentes ao perfil do usuário e inclui um botão "Logoff" que redireciona de volta à página de login.

Resumo das funções principais deste código:

getUserProfileFromURL():

Esta função é responsável por extrair o perfil do usuário da URL da página atual. Ela utiliza o objeto URLSearchParams para analisar os parâmetros da URL e retorna o valor do parâmetro perfil.
displayProducts(profile):

Esta função recebe o perfil do usuário como parâmetro e é responsável por exibir os produtos correspondentes ao perfil do usuário na página. Ela acessa a lista de produtos do objeto products com base no perfil fornecido e gera o HTML para exibir os produtos na página.
displayGreetingAndThankYou(profile):

Esta função recebe o perfil do usuário como parâmetro e é responsável por exibir uma saudação personalizada e uma mensagem de agradecimento na página de produtos. Dependendo do perfil do usuário, uma saudação específica e uma mensagem de agradecimento são definidas. Essas mensagens são então exibidas em elementos HTML específicos na página.
window.onload:

O código dentro desta função é executado quando a página é totalmente carregada. Ele obtém o perfil do usuário da URL, chama as funções displayGreetingAndThankYou(profile) e displayProducts(profile) para exibir a saudação, agradecimento e produtos correspondentes na página.
Essas funções trabalham juntas para criar uma experiência personalizada na página de produtos, exibindo uma saudação específica para cada usuário e mostrando os produtos adequados ao perfil do usuário.
________________________________________________________________________________________________________________________
login.html é a página de login onde o usuário pode inserir suas credenciais. Quando o login é bem-sucedido, ele é redirecionado para a página de produtos correspondente ao seu perfil.

Resumo:

Definição de Dados de Usuários:

O array users contém objetos que representam os usuários e suas credenciais. Cada objeto possui propriedades para username, password e perfil.
Função de Login:

A função login() é chamada quando o usuário clica no botão de login. Ela obtém os valores dos campos de entrada de nome de usuário e senha.
Em seguida, utiliza o método find() para buscar um usuário nos dados de users cujo nome de usuário e senha correspondem aos fornecidos pelo usuário.
Se um usuário autenticado for encontrado, o navegador é redirecionado para a página de produtos correspondente ao perfil do usuário usando window.location.href.
Caso contrário, exibe um alerta informando que o nome de usuário ou senha está incorreto.
Essa parte do código é responsável por autenticar os usuários com base nas credenciais fornecidas e redirecioná-los para a página de produtos adequada após o login bem-sucedido.
________________________________________________________________________________________________________________________
