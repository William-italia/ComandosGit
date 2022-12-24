 #  GIT FUNDAMENTAL 
 
## -  O que é o GitHub?


* É um serviço para gerenciar repositórios, gratuito e amplamente utilizado;
* Podemos enviar nossos projetos para o GitHub e disponibilizá-lo para outros devs;
* O GitHub é gratuito tanto para projetos públicos como privados;

<br>

## - O que é um repositório?

* É onde o código será armazenado;
* Na maioria das vezes cada projeto tem um repositório;
* Quando criamos um repositórioestamos iniciando um projeto; 
* O repositorio pode ir para servidores que são especializados em gerenciar repos, como: GitHub e Bitbucket;
* Cada um dos desenvolvedores do time pode baixar o repositório e criar versões diferentes em sua máquina;

<br>

## - Criando repositório
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

## - Enviando repositório para o GitHub

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

## - Verificando mudanças do projeto 

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

## - Adicionando arquivos ao projeto

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

## - Salvando alterações do projeto

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

## - Enviando código ao repo remoto

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

## - Recebendo as mudanças

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

## - clonando repositórios 

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

## - Removendo arquivos do repositório

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

## - Histórico de verificações

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

## - Renomeando arquivos 

* Com o comando: GIT MV podemos renomear um arquivo ou movelo;
* O mesmo também pode ser movido para outra pasta;
* E isso fará com que este novo arquivo seja monitorado pelo git;
* O arquivo anterior é excluido
<br>
<br>

`````
COMANDOS: 

> git mv
> git mv about.html 
>
`````


