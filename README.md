Este texto foi elaborado na minha máquina usando o Gedit.


GIT 

//Versão do Git 
git --version 

//Setar o nome de usuario
git config --global user.name "Gabriel Rezende"

//Setar o email
git config --global user.email "gabrielcastrorezende@gmail.com"

//Listar as configs 
git config --list

//Iniciar repositório
git init

//Verificar alterções
git status

//Adicionar vários arquivos ou apenas um
git add --all | git add -A | git add .
git add arquivo.file

//Adicionar arquivos não siginifica que ele foi salvo, status no console fica: "Changes to be commited"

//Salvar arquivos significa commitar
git commit -m "Mensagem desejada"

//Untracked files: Significa que o arquivo ainda não foi adicionado 
//Chanages not staged for commit: Significa que o arquivo adicionado e commitado sofreu algum tipo de alteração. 

FLUXO DO GIT: 
1 - Working Directory: 
	- Arquvios criados, excluidos e adicionados 
2 - Staging Area: 
	- Arquivos adicionados e preparados para serem versionados 
	- git add . 
	- git add -A
	- git add --all 
	- git add arquivo.file
3 - Commited: 
	- Arquivos salvos 
	- git commit -m "Mensagem identificando alteração"

//Quando os arquivos são deletados, o git também identifica

//Para saber a diferença da versão atual para a anterior
git diff 
git diff -cached
git diff -staged 

//Listar todos os commits feitos no meu projeto 
git log 
	Estutura:
	- comit id unico
	- autor 
	- dia 
	- mensagem 
	
git log --oneline 
	Para visualizar em uma linha, de maneira mais resumida 
	
//Caso queira voltar para alguma versão de commit anterior 
git checkout "primeiros caracteres do commit desejado"
	- Util em caso de crashar e precisar de voltar a versão 
	
//O git checkout nos leva a uma branch com o código informado, caso queiramos voltar par o último commit, devemos usar 
git checkout nome_da_branch

//Caso eu tenha feita uma alteração no arquivo e queira voltar ao commit da header - desfazer alterações
git checkout arquivo.file
	- Para arquivos específicos
git reset --hard 
	- Desfazer TODAS as mudanças em diversos arquivos

//Caso o arquivo esteja no status de Working, aonde não foi arquivado
git clean -f

//O arquivo .gitignore exclui tipos especificos (*.type) de arquivo ou arquivos especificos 
	
//Para clonar um repositório local ou online
git clone local/ nome_da_pasta

//Arquivo de marcação para disponibilizar e otimizar a descrição 
README.md 

//Comando que envia as alterações para o repositório online 
git push 

//Comando que recebe as alterações feitas no repositório
git pull 

//Fork um repositório de terceiro clona para o seu perfil no github, logo após você pode clonar para a sua máquina local. 

//Após as mudanças no seu fork, você pode solicitar um pull request e assim modificar o repositório de terceiros. 

//Aba Issues para identificar um problema e informar ao proprietário do repositório. 

//Milestone indica em qual versão o projeto irá consertar o issue requirido.

//Labels é uma tag identificando o tipo de Issue. 

//Branch é uma ramificação do código para implementar funcionalidades separadamente sem que atinjam funcionalidades estáveis no projeto. 

//Para listar as branch que temos no nosso repositório local
git branch 

//Para criar uma nova branch 
git branch nomeBranch

//O terminal irá dispor uma * na branch em que estamos. 

//Caso queira mudar de branch
git checkout nomeBranch 

//Para criar uma nova branch e mudar para mesma 
git checkout -b nomeBranch 

//Para adicionar uma nova branch no GitHub 
git push -u origin nomeBranch 

//Para remover uma branch 
git branch -d nomeBranch 

//Caso tenha deletado a branch localmente e queira voltar.
git checkout nomeBranch 

//Para excluir uma branch remota
git push --delete origin nomeBranch 

//Para alterar o nome da branch, saia dela 
git branch -m branchNome branchNovoNome

//Caso tenha feito uma alteração em uma branch e quero mergear as duas branches 
git branch nomeBranchComAlteracao
	- Neste comando, o código já commita 
	
//Para adicionar e commitar junto 
git commit -a -m "mensagem"

//Na aba pull-request, é útil para fazer a revisão de código antes dele ser mergeado 

//Para criar tags
git tag -a "nome" -m "descrição"

//Para remover tags localmente 
git branch -D tag

//Para remover tags remotamente 
git push --delete origin tag 

//Reverter um commit n vezes
git reset --hard HEAD~n

//Pra saber as URLs associadas 
git remote -v 


