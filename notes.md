#

# Uso do Git no dia-a-dia

![uso-basico-git-dia-a-dia](/images/uso-basico-git-dia-a-dia.jpg)

* ```git clone ‹URL do repositório>``` Comando para baixar ou clonar o código-fonte existente de um repositório remoto (como, por exemplo, o Github).
* ```git checkout ‹nome da branch>``` Um dos comandos mais usados. É utilizado, na maioria dos casos, para trocar de uma branch para outra.
* ```git add``` Usado para incluir as alterações de vários arquivos em nosso próximo commit.
* ```git add <arquivo>``` Usado para incluir as alterações de vários um único arquivo em nosso próximo commit.
* ```git status``` Fornece todas as informações necessárias sobre a branch atual.
* ```git commit -m "mensagem do commit"``` Talvez o comando mais usado do Git. Serve como um ponto de verificação no processo de desenvolvimento, onde você adiciona uma breve mensagem e pode voltar a esse ponto mais tarde para verificar, se necessário.
* ```git push``` Esse comando faz o upload dos seus commits no repositório remoto.
* ```git pull ‹ repositório remoto>``` Usado para obter as atualizações de um repositório remoto e aplica-las em seu espaço de trabalho local.
* ```git merge < commit id›``` Esse comando, basicamente, mescla todas as atualizações do seu repositório local com o diretório de trabalho atual.

# Dicas para o arquivo readme

* O que deve conter no arquivo readme:
    * Descrição do projeto;
    * Funcionalidades;
    * Como os usuários podem utilizá-lo;
    * Onde os usuários podem encontrar ajuda sobre o projeto;
    * Autor(es) do projeto.
    * Título e imagem de capa;
    * Badges (que na tradução literal é distintivo, emblema ou insígnia). Seus objetivos são indicar o estado atual do projeto, licença caso tenha, versões, dependências, testes e entre outros. Vide imagem abaixo: ![badges](/images/badges.png)
        * Caso queira fazer suas badges, você pode utilizar o [shields.io](https://shields.io/). Ele fornece na página principal, diversos exemplos. Na caixa de texto inicial desse site, você pode colar o link do repositório do projeto no GitHub, para que ele sugira, automaticamente, algumas badges que podem ser utilizadas no projeto, fornecendo o link da Badge para copiar e colar no seu readme, conforme a imagem abaixo: ![shields-io](/images/shields-io.png)
    * Índice;
    * Descrição do projeto;
    * Status do projeto;
    * Funcionalidades e demonstração da aplicação;
    * Acesso ao projeto;
    * Tecnologias utilizadas;
    * Pessoas contribuidoras;
    * Pessoas desenvolvedoras do projeto;
    * Licença.
