# Git e GitHub

* Para instalar o Git, basta clicar em “next”, “next”, “next”...
* Iniciar um repositório:
* Na pasta selecionada, clique com o botão direito e selecione "Open Git Bash here” para abrir o terminal próprio do Git, conforme a imagem abaixo:
* ![open-git-bash-here](/images/open-git-bash-here.jpg)
* ```git init``` inicia um repositório na pasta selecionada, conforme a imagem abaixo:
* ![git-init](/images/git-init.jpg)
* Isso cria uma pasta oculta chamada ".git", conforme a imagem abaixo:
* ![pasta-oculta-git](/images/pasta-oculta-git.jpg)
* ```git status``` exibe o status do repositório e também quais arquivos já foram ou não incluídos no controle de versão, conforme a imagem abaixo:
* ![git-status-1](/images/git-status-1.jpg)
* ```No commits yet``` informa que não há versões do código, conforme a imagem acima:
* ```Untracked files:``` informa que existem arquivos que não estão no controle de versão e quais arquivos são esses, conforme a imagem acima.
* ```git add “nome do arquivo.extensao”``` adiciona o arquivo no controle de versão, conforme a imagem abaixo:
* ![git-add-1](/images/git-add-1.jpg)
* Ao rodar o comando ```git status``` novamente, ele exibirá o arquivo incluído recentemente ao controle de versão, conforme a imagem abaixo:
* ![git-status-2](/images/git-status-2.jpg)
* ```git add .``` adiciona todos os arquivos contidos na pasta ao controle de versão.
* ![git-add-2](/images/git-add-2.jpg)
* Após adicionar os arquivos ao controle de versão, é necessário criar uma versão antes de disponibilizá-lo no GitHub (ou qualquer outro).
* O comando ```git commit –m“mensagem”``` criaram a primeira versão do repositório.
* No local do ```“mensagem”```, após o ```–m``` é necessário adicionar a mensagem do porque foi criado essa versão (commit) do código.
* Ao rodar esse comando pela primeira vez, será pedido que configure o Git na máquina.
* ```$ git config --global user.email fulanodetal@exemplo.br```
* ```$ git config --global user.name "Fulano de Tal"```
* Deverão ser utilizados os mesmos dados da conta no GitHub .
* Essa informação é importante porque o nome ficará atrelado a cada versão (commit) enviado.
* ![git-push-1]ch/images/git-push-1.jpg)
* ![git-commit-m-mensagem](/images/git-commit-m-mensagem.jpg)
* Após rodar o comando ```git commit –m“mensagem”``` serão exibidas as seguintes informações, conforme a imagem abaixo:
* Nome do commit;
* Nome da branch para onde foram enviadas essas alterações. No caso, foi a branch master.”;
* Arquivos adicionados à versão;
* ![arquivos-adicionados-versao](/images/arquivos-adicionados-versao.jpg)
* ```git push``` envia as alterações para o servidor na nuvem.
* É necessário a definição do local onde será enviado, caso contrário, poderá haver um erro.
* Nesse caso deve-se acessar o GitHub e criar um repositório. Após criar o repositório através do site do GitHub , basta copiar o link do mesmo (https://github.com/diechojoroque/curso-chit-github-devaprender) para o terminal bash do Git.
* ```git remote add origin https://github.com/dichgojoroque/cursochgit-github-devaprender``` define o local onde o código será enviado.
* ![git-remote-add-origin](/images/ git-remote-add-origin.jpg)
* Após isso, execute novamente o comando ```git push```. Ocorrerá um erro porque ainda não foi definida qual a branch ele deverá enviar o código.
* ![git-push-2](/images/git-push-2.jpg)
* ```git reflog``` exibe o histórico de atualizações do código, em ordem decrescente de versões.
* ![git-reflog](/images/git-reflog.jpg)
* ```git reset –hard id-version``` (onde ```id-version``` será por ex.: ```c0bf19b```) retorna para a versão desejada do código. Esse comando permite navegar entre as versões do código.
* Pull request é utilizado no site do GitHub após o envio das atualizações.
* ![pull-request](/images/pull-request.jpg)
* Após clicar em “Compare & pull request”, basta informar o qual irá juntar com qual branch.
* ![compare-pull-request](/images/compare-pull-request.jpg)
* Após isso, poderá ser descrito o que foi feito além do nome do commit.
* ![nome-commit](/images/nome-commit.jpg)
* Na aba à lateral direita é possível verificar o menu “reviewrs” que são as pessoas que revisarão os seus projetos. Caso a atualização seja reprovada, basta verificar os comentários, realizar as alterações e enviar um novo commit, não sendo necessário enviar um novo pull request. Basta enviar um comentário comentando o nome dos revisores que não aprovaram a nova versão, dizendo que realizou as alterações solicitadas.
* ![comentario](/images/comentario.jpg)
* ```touch .gitignore``` cria um arquivo .gitignore no repositório do projeto.
* Após criado, abra o arquivo através do notepad para definir os arquivos a serem ignorados.
* ![gitignore](/images/gitignore.jpg)
* Após isso, execute os comandos ```git add .```, ```git status```, ```git commit –m”tituloCommit”``` e ```git push``` para adicionar o arquivo .gitignore ao repositório.
* Resumo:
* ![resumo](/images/resumo.jpg)
* Vocabulário:
* commit é versão do código;
* branch (ramo) são divisões ou versões diferentes do código que está sendo versionado de forma separada. Inicialmente, enviaremos sempre para a master, logo, você deverá executar o comando sugerido: ```git push --set-upstream origin master```. Após executar esse comando, aparecerá uma janela para realizar login, caso ainda não o tenha realizado. Feito o login, o comando fará o envio do código ao GitHub .
* ![branch-1](/images/branch-1.jpg)
* Ao retornar à página do GitHub e atualizá-la, será exibida uma mensagem informando que houveram envios recentes “master had recent pushes 1 minute ago”. Basta mudar da branch main para branch master para acessar o código.
* Em projetos onde mais de uma pessoa trabalha ou aqueles já utilizados por clientes, é comum deixar um branch com a versão estável e outras branchs onde são inseridas as edições e melhorias antes de serem enviadas para a versão estável.
* ![branch-2](/images/branch-2.jpg)
* ```git branch``` exibe as branchs disponíveis.
* ![git-branch](/images/git-branch.jpg)
* O * e a cor verde no nome indicam qual a branch em uso, atualmente.
* ```git branch nomeASerUsado``` onde ```nomeASerUsado``` será o nome da branch. Esse comando é utilizado para a criação de uma nova branch.
* ![git-branch-nome-a-ser-usado](/images/git-branch-nome-a-ser-usado.jpg)
* "Staging” é comumente utilizado para branchs de desenvolvimento, testes e afins.
* ```git checkout Diego``` é utilizado para mudar para a branch citada no comando.
* ![git-checkout-1](/images/git-checkout-1.jpg)
* Para unir as alterações realizadas em branchs diferentes, você deverá ir na branch que receberá a nova versão ```git branch master``` e depois executar o comando ```git merge staging```.
* Antes de realizar a união (merge) dos códigos, recomenda-se fortemente a execução do comando ```git pull```, para trazer à máquina a versão mais recente disponível do código, no repositório.
* ![git-pull-1](/images/git-pull-1.jpg)
* ![git-pull-2](/images/git-pull-2.jpg)
* ```git checkout –b nomeASerUtilizado master``` é usado para sair da branch atual para a branch a ser criada em um único comando e o ```master``` é o nome da branch utilizada como base para a criação da nova branch.
* Conforme a imagem abaixo, será exibida as alterações realizadas.
* Lembre-se sempre de utilizar o comando ```git push``` para enviar as alterações ao servidor, no caso, para o GitHub.
* ![git-checkout-2](/images/git-checkout-2.jpg)
* ![master](/images/master.jpg)
* Continuar em "Como verificar histórico de atualizações" (22'33").

# Uso do Git no dia-a-dia

![uso-basico-git-dia-a-dia](/images/uso-basico-git-dia-a-dia.jpg)

* ```git clone ‹URL do repositório>``` Comando para baixar ou clonar o código-fonte existente de um repositório remoto (como, por exemplo, o GitHub);
* ```git checkout ‹nome da branch>``` Um dos comandos mais usados. É utilizado, na maioria dos casos, para trocar de uma branch para outra;
* ```git add``` Usado para incluir as alterações de vários arquivos em nosso próximo commit;
* ```git add <arquivo>``` Usado para incluir as alterações de um único arquivo em nosso próximo commit;
* ```git status``` Fornece todas as informações necessárias sobre a branch atual;
* ```git commit -m "mensagem do commit"``` Talvez o comando mais usado do Git. Serve como um ponto de verificação no processo de desenvolvimento, onde você adiciona uma breve mensagem e pode voltar a esse ponto mais tarde para verificar, se necessário;
* ```git push``` Esse comando faz o upload dos seus commits no repositório remoto;
* ```git pull ‹repositório remoto>``` Usado para obter as atualizações de um repositório remoto e aplica-las em seu espaço de trabalho local;
* ```git merge <commit id›``` Esse comando, basicamente, mescla todas as atualizações do seu repositório local com o diretório de trabalho atual.

# Dicas para o arquivo readme

* O que deve conter no arquivo readme:
	* Descrição do projeto;
	* Funcionalidades;
	* Como os usuários podem utilizá-lo;
	* Onde os usuários podem encontrar ajuda sobre o projeto;
	* Autor(es) do projeto;
	* Título e imagem de capa;
	* Badges (que na tradução literal é distintivo, emblema ou insígnia). Seus objetivos são indicar o estado atual do projeto, licença caso tenha, versões, dependências, testes e entre outros. Vide imagem abaixo:
		![badges](/images/badges.jpg)
		* Caso queira fazer suas badges, você pode utilizar o [shields.io](https://shields.io/). Ele fornece na página principal, diversos exemplos. Na caixa de texto inicial desse site, você pode colar o link do repositório do projeto no GitHub , para que ele sugira, automaticamente, algumas badges que podem ser utilizadas no projeto, fornecendo o link da Badge para copiar e colar no seu readme, conforme a imagem abaixo:
			![shields-io](/images/shields-io.jpg)
	* Índice;
	* Descrição do projeto;
	* Status do projeto;
	* Funcionalidades e demonstração da aplicação;
	* Acesso ao projeto;
	* Tecnologias utilizadas;
	* Pessoas contribuidoras;
	* Pessoas desenvolvedoras do projeto;
	* Licença.
