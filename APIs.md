- Login
	1) Cadastro
		- POST ``cadastrarUsuario(login, email, senha)``
	2) Autenticação
		- POST ``autenticaUsuario(login, senha)``
	3) Esqueci minha senha
		- POST ``recuperaSenha(email, login, novaSenha)``

4) Pagina principal ([basei-me aqui](https://www.petfinder.com/search/dogs-for-adoption/vi/saint-croix-island/))
	- GET ``buscaTodosPets()`` --> filtro na URL ou no body da requisição?
	- GET ``buscaPetFiltros(categoria, especie, porte, sexo, data, localizacao, nome)``

5) Página do Pet (essa atela mostra informações do pet )
	- GET ``buscaPet(IDdoPet)``

6) Perfil CRUD:
	- PUT ``updateDados(IDpessoa)``
	- POST ``adicionaPet(IDPessoa, Pet)`` *--> Aqui adicionar só o pet do dono ou qualquer um?*
	- GET buscaPets(IDPessoa)
	- PUT editarPet(IDPessoa, IDpet)

7) e 8. Pet CRUD:
	- POST ``adicionaPet(foto, tipo, porte, sexo, categoria, localizacao, descricao, contato)``
	- PUT ``editaPet(idPet, json do que é para alterar)``
	- POST ``excluiPet(idPet)`` --> *aqui seria bom adicionar um status 'ativo' sim/não para não excluir o pet da plataforma. Só inativa ele para que ele não apareça mais.*
	- POST ``mudaStatus(IDpet, status)``

___
- Extra:
	- Login
		- Login com Google e Facebook
	- Página do pet
		- POST ``postarComentario(IDdoPet)`` --> *se adequar à API do Disqus*
