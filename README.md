 #  GIT FUNDAMENTAL 
 
### -  O que é o GitHub?


* É um serviço para gerenciar repositórios, gratuito e amplamente utilizado;
* Podemos enviar nossos projetos para o GitHub e disponibilizá-lo para outros devs;
* O GitHub é gratuito tanto para projetos públicos como privados;

<br>

### - O que é um repositório?

* É onde o código será armazenado;
* Na maioria das vezes cada projeto tem um repositório;
* Quando criamos um repositórioestamos iniciando um projeto; 
* O repositorio pode ir para servidores que são especializados em gerenciar repos, como: GitHub e Bitbucket;
* Cada um dos desenvolvedores do time pode baixar o repositório e criar versões diferentes em sua máquina;

<br>

### - Criando repositório
* Para criar um repositório utilizamos o comando GIT INIT;
* Desta meneira o git vai criar os arquivos necessarios para inicializá-lo;
* Que estão na pasta oculta .git;
* Após este comando o diretório atual será reconhecido pelo git como um projeto e responderá aos seus demais comandos;
<br>
<br>

````
COMANDOS: 

> git init
````
<br>

### - Enviando repositório para o GitHub

* Podemos facilmente enviar nossos repos para o GitHub;
* Precisamos criar o projeto no nosso GitHub e inicializarmos o mesmo no git em nossa máquina, sincronizar com o github e enviar;
* E esta sequêcia que parece ser complexa é facilmente executada por poucos comandos;
* Vale lembrar que só fazemos UMA VEZ POR PROJETO esse fluxo;
* Porém alguns dos comandos utilizados vão ser úteis ao longo dos seus projetos;
<br>
<br>

````
COMANDOS:

> git remote -v (mostra a origem atual do projeto); 
> git remote add origin <link ou ssh do repo do projeto> (add uma origem ao projeto);
> git remote rm origin (remove a origem atual do projeto)
> usamos git push -u origin main no primeiro push do projeto (quando fazemos o repo desse modo);
````

<br>

### - Verificando mudanças do projeto 

* As mudanças do projeto podem ser verificadas por: GIT STATUS;
* Este comando é utilizado frequentemente durante um projeto
* Aqui serão mapeadas todas as alterações do projeto;
* Podemos também dizer que é a diferença do que já foi enviado para o servidor ou salvo no projeto;
<br>
<br>

````
COMANDOS:

> git status
````

<br>

### - Adicionando arquivos ao projeto

* Para adicionarmos arquivos novos a um projeto utizamos o comando: GIT ADD;
* Podemos adicionar um arquivos específico como também diversos de uma só vez;
* Somente adicionando arquivos eles serão monitorados pelo git;
* É interessante utilizar este comando de tempos em tempos para não perder algo importante por descuido;
<br>
<br>

````
COMANDOS:

> git add . (adiciona todos os arquivos e modificações feitas);
> git add <nome.tipo> (adiciona um arquivo especifico);
````
<br>

### - Salvando alterações do projeto

* As alterações salvas do projeto asão realizadas por: GIT COMMIT;
* Podemos commitar arquivos específicos ou vários de uma vez com a flag -a;
* É uma boa prática enviar uma mensagem a cada commit, com as alterações que foram feitas;
* A mensagem pode ser adiciomada usando a flag -m;
<br>
<br>

````
COMANDOS: 

> git commit 
> git commit -m "mensagem"
> git commit -a -m "mesagem"
> git commit -a -m "mensagem
>>
>> descrição da mensagem" 
````
<br>

### - Enviando código ao repo remoto

* Quando finalizamos uma funcionalidade nova, enviamos o código ao repositório remoto, que é o código-fonte;
* Está ação é feita pelo comando: GIT PUSH;
* Após está ação o código do servidor será atualizado baseando-se no código local enviado;
<br>
<br>

````
COMANDOS:

> git push
````
<br>

### - Recebendo as mudanças

* É comum também ter que sincronizar o repo local com as mudanças do remote;
* Está ação é feita pelo comando: GIT PULL;
* Após o comando serão  buscadas atualizações, se encontradas elas serão unidas ao código atual existente na nossa máquina;
<br>
<br>

````
COMANDOS:

> git pull
````
<br>

### - clonando repositórios 

* O ato de baixar um repositório de um servidor remoto é chamado de clonar repositório;
* Para esta ação utilizamos git clone;
* Passando a referência do repositório remoto;
* Este comando é utilizado quando entramos em um novo projeto, por exemplo
* Para realizarmos o clone utilizamos o comando GIT CLONE (link ou ssh do repositorio);
<br>
<br>

````
COMANDOS: 

> git clone https://github.com/user/repo.git ou git@github.com:user/repo.git
> git clone https://github.com/user/repo.git . (usando o ponto ele clonara o repo no diretório atual)
> git clone https://github.com/user/repo.git projeto01 (usando um nome ele criara um clone com o nome desejado no caso "projeto01")
````
<br>

### - Removendo arquivos do repositório

* Os arquivos podem ser deletados da monitoração do git;
* O comando para deletar é git rm
* Após deletar um arquivo do git ele não terá mais suas atualizações consideradas pelo git;
* Apenas quando for adicionado novamente pelo comando git add;
<br>
<br>

````
COMANDOS:

> git rm <nome>
````
<br>

### - Histórico de verificações

* Podemos acessar um log de modificações feitas no projeto;
* O comando para este recurso é: GIT LOG;
* Você receberá uma informação dos commits realizados no projeto até então;
<br>
<br>

`````
COMANDOS:

> git log
`````
<br>

### - Renomeando arquivos 

* Com o comando: GIT MV podemos renomear um arquivo ou movelo;
* O mesmo também pode ser movido para outra pasta;
* E isso fará com que este novo arquivo seja monitorado pelo git;
* O arquivo anterior é excluido
<br>
<br>

`````
COMANDOS: 

> git mv
> git mv aboult.html html/aboult.html
> git mv abouuut.html aboult.html
`````
<br>

### - Desfazendo alterações 

* O arquivo modificado pode ser retornado ao estado original
* O comando utilizado é o: GIT CHECKOUT;
* Após a utilização do mesmo o arquivo sai do staging;
* Caso seja feita uma proxima alteraçãos, ele entra em stading novamente;
<br>
<br>

`````
COMANDOS:

> git checkout (volta para o ultimo push)
> git checkout html/aboult.html (tambem pode ser usado em um arquivo especifico, dependendo da situação é recomendavel esse formato)
`````
<br>

### - Ignorando arquivos do projeto

* Uma técnica mmuito utilizada é ignorar arquivos do projeto;
* Devemos inserir um arquivo chamado .gitignore na raiz do projeto;
* Nele podemos inserir todos os arquivos que não devem entrar no versionamento;
* Isso é útil para arquivos gerados automaticamente ou arquivos que contêm informações sensíveis;
<br>
<br>

### - Desfazendo todas as alterações 

* Com o comando: GIT RESET podemos resetar as mudanças feitas;
* Geralmente é utilizado com a flag --hard
* Todas as alterações commitadas e também as pendentes serão excluidas;
<br>
<br>

`````
COMANDOS: 

> git reset --hard origin/main 
(git reset --hard origin/branch desejada geralmente usa-se a main)
`````
<br>

# TRABALHANDO COM BRANCHES

### - O que é um branch?

* Branch é a forma que o git separa as versões dos projetos;
* Quando um projeto é criado ele inicia na branch main, estamos trabalhando nela até este ponto;
* Geralmente cada nova feature de um projeto fica em um branch separado;
* Após a finalização das alterações os branchs são unidos para ter o código-fonte final;
<br>
<br>

### - Criando e visualizando os branches

* Para vizualizar os branchs disponíveis basta usar o comando: GIT BRANCH;
* Para criar um branch você precisa utilizar o comando: GIT BRANCH nome;
* Estas duas operações são muito utilizadas no dia a dia de um dev;
<br>
<br>

`````
COMANDOS:

> git branch (mostra as branchs existentes no projeto)
> git branch <nome> (cria uma nova branch)
`````
<br>

### - Deletando branchs

* Podemos deletar um branch com a flag -d ou --delete;
* Não é comum deletar um branch, normalmente guardamos o histórico do trabalho;
* Geralmente se usa o delete quando o branch foi criado errado;
<br>
<br>

`````
COMANDOS:

> git branch -d <nome_da_branch>
> git branch --delete <nome_da_branch>
`````
<br>

### - Mudando de branch 

* Podemos mudar para outro branch utilizando o comando: GIT CHECKOUT nome da branch;
* Este comando também é utilizado para dispensar mudanças de um arquivo;
* Alterando o branch podemos levar alterações que não foram commitadas junto, tome cuidado!;
<br>
<br>

`````
COMANDOS:

> git checkout <nome-da-branch-existente> (muda a branch para uma já existente)
> git checkout -b <"nome-da-branch"> (cria e muda de branch ao mesmo tempo)
`````
<br>

### - Unindo branches

* O código de dois branches distintos pode ser unido pelo comando: GIT MERGE <"NOME">
* Outro comando para a lista dos mais utilizados;
* Normalmente é por meio dele que recebemos as atualizações de outros devs;
<br>
<br>

`````
COMANDOS: 

> git merge <nome-da-branch> (unifica as branches)
`````
<br>

### - Stash

* Podemos salvar as modificações atuais para prosseguir com uma outra abordagem de solução e não perder o código;
* O comando para esta ação é o: GIT STASH;
* Após o comando o branch será resetado para a sua versão de acordo com o repositório, ultimo git push;
<br>
<br>

 `````
 COMANDOS: 

 > git stash (deixa o arquivo de acordo com o repo remoto, mas salva o codigo apagado em uma stash)
 `````
<br>

### - Recuperando stash

* Podemos verificar as stashs criadas pelo comando GIT STASH LIST;
* E também podemos recuperar a stash com o comando GIT STASH NOME;
* Desta maneira podemos continuar de onde paramos com os arquivos adicionados a stash
<br>
<br>

````
COMANDOS:

> git stash list (lista as stashs existentes)
> git stash apply <numero-da-stash> (recupera a stash)
> git stash show -p <numero-da-stash> (mostra as diferenças de uma determinada stash com a atual no terminal)
````
<br>

### - Removendo a stash 

* Para limpar totalmente as stash de um branch podemos utilizar o comando GIT STASH CLEAR;
* caso seja necessário deletar uma stash específica podemos utilizar GIT STASH DROP numero-da-stash;
<br>
<br>

`````
COMANDOS:

> git stash clear (apaga todas as stashs existentes)
> git stash drop number (apaga uma determinada stash)
`````
<br>

### - Utilizando tags

* Podemos criar tags nos branches por meio do comando GIT TAG -A NOME -M "mensagem"
* A tag é diferente do stash, serve como um checkpoint de um branch;
* É utilizada para demarcar estágios do desenvolvimento de algum recurso;
<br>
<br>

`````
COMANDOS: 

> git tag (lista as tag existentes)
> git tag -a <nome> -m <"msgm"> (cria uma tag)
`````
<br>

### - Verificando e alterando tags

* Podemos verificar uma tag com o comando GIT SHOW NOME;
* Podemos trocar de tags com o comando GIT CHECKOUT NOME;
* Desta maneira podemos retroceder ou avançar em checkpoints de um branch;
<br>
<br>

`````
COMANDOS:

> git show nome-da-tag (mostra o conteúdo da tag)
> git checkout nome-da-tag (muda de tag)
`````
<br>

### - Enviando e compartilhando tags

* As tags podem ser enviadas para o repositório de código, sendo compartilhada entre os devs;
* O comando é GIT PUSH NOME;
* Ou se você quiser enviar mais tags GIT PUSH ORIGIN --TAGS;
<br>
<br>

````
COMANDOS:

> git push origin nome-da-tag (envia uma tag especifica ao repositório)
> git push origin --tags (envia todas as tags existentes na branch ao repositório)
````
<br>

# COMPARTILHAMENTO E ATUALIZAÇÃO

### - Encontrando branches

* Branches novas são criadas a todo tempo e o seu git pode não estar mapeando eles;
* Com o comando: GIT FETCH você é atualizado de todos os branchs e tags que ainda não estão sendo reconhecidas pelo seu git; 
* Este comando é útil para utilizar o branch de algum outro dev do time por exemplo;
<br>
<br>

````
COMANDOS:

> git fetch -a (puxa todos os branches que estão remotos)
````
<br>

### - Recebendo alterações

* O comando GIT PULL serve para recebermos atualizações do repositório remoto;
* Cada branch pode ser atualizado com o GIT PULL; 
* Utilizamos tanto para atualizar a main do repo como também quando trabalhamos em conjunto e queremos receber as atualizações de um dev;
<br>
<br>`

 ````
 COMANDOS: 

 > git pull (atualiza seu repo local com o remoto)
 ````
<br>

### - Enviando alterações 

* O comando GIT PUSH faz o inverso do pull, ele envia as alterações para o repo remoto;
* Serve também para enviar as atualizações de um branch específico para um outro dev;
* Ou quando terminamos uma tarefa e precisamos enviar ao repo;
<br>
<br>

````
COMANDOS:

> git push
````
<br>

### - Utilizando o remote  

* Com o GIT REMOTE podemos fazer algumas ações como: adicionar um repo para trackear ou remover; 
* Quando criamos um repo remoto, adicionamos ele ao git  com GIT REMOTE ADD ORIGIN LINK
<br>
<br>

````
COMANDOS:

> git remote 
> git remote -v (mostra as origins atuais do repo)
> git remote rm origin  (remove a origem do repo)
> git remote add oring <link> (adiciona origem para o repo)
````
<br>

### - Trabalhando com submódulos

* Submódulo é a maneira que temos de possuir dois ou mais projetos em um só repositório;
* Podemos adicionar uma dependência ao nosso projeto atual, porém mantendo suas estruturas separadas;
* Para adicionar o submódulo utilizamos o comando GIT SUBMODULE ADD REPO;
* Para verificar os submódulos o comando é: GIT SUBMODULE;
<br>
<br>

````
COMANDOS:

> git submodule (mostra os submodulos existentes no repo)
> git submodule add link-do-repo diretorio (cria um submodulo) 
````
<br>

### - Atualizando submódulo

* Para atualizar um submódulo primeiro devemos commitar as mudanças;
* E para enviar para o repo do submódulo utilizamos GIT PUSH --RECURSE-SUBMODULES=ON-DEMAND;
* Este fluxo fará a atualização apenas do submódulo;
<br>
<br>

````
COMANDOS:

> git push --recurse-submodules=on-demand (esse modelo de git push é utilizado para atualizar submódulos)
````
<br>

# Análises e inspeção 