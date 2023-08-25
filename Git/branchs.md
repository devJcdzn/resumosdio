# Trabalhando com Branches
  
### Criando ua nova branche
  
Muitas vezes quando estamos trabalhando em projetos reais, precisamos de testar
alterações e/ou novos recursos em nossa aplicação ou sistema. Entretanto, não queremos
que essas alterações sejam enviadas diretamente para a aplicação, podendo gerar bugs
ou inconsistências o que seria desagradável para os usuários.
Então, como solução, podemos criar uma camada de teste, paralela à nossa camda principal
para que dessa vez, possamos testar essas alterações sem afetar a aplicçao final.
  
Esse conceito é muito utilizado e importante, em qualquer tipo de produção, seja Web, 
Desktop ou mobile. Por isso, temos que entender muito bem como as branches do git funcionam
e vamos começar pela criação e manipulação.
  
- Para criar branches através de uma linha de comando, usamos `git checkou -b branchName`.
  Com isso, importante saber que quando criamos uma nova branch ela aponta para o ultimo commit da branch anterior.
  
- Se fizermos um novo commit na branch nova, e em segida dermos um 'git log', de cara, 
  perceberemos que a somente branch recém-criada apontará para esse commit.

- Para retornarmos a nossa branch anterior, a branch main, podemos usar `git checkout 'main'`
  assim podemos perceber, que em nosso repositório local, os arquivos referentes a nova branch
  não existirão na main, pois, elas são idependentes agora. Assim, toda alteração feita em uma
  branch idependente, não afetará de maneira alguma a principal.  
  
##
### Manipulação básica das branches  
##
> Ao usar o comando `git branch -v` podemos ver todas as branches do repositório e estará destacada
a que você está no momento.
##
Para que as alterações feitas em sua nova branche sejam aplicadas na *main* podemos mescla-las
usando o `git merge branchName`. Assim as camadas serão unidas.  
Depois de já ter adcionado as alterações desejadas na main, não há mais necessidade dessa branch
paralela, então podemos **deleta-la** usando `git branch -d branchName`.
##
### Conflitos de Merge  

Uma situação comum para quem trabalha em equipe são os *conflitos de merge*. Supondo que você
e um colega de trabalho estejam trabalhando em um mesmo repositório, alteram a mesma linha de 
código e isso gera uma "concorrência", ao tentat enviar, o git não reconhece qual deve ser mantida 
como preferência. Por isso devemos ter uma boa noção de como trabalhar com isso.  

- Tendo em mente que o conflito foi causado por alterações em mesmo trecho, porém diferentes entre si
  ao tentarmos enviar para o repositório remoto, recebemos uma error message, indicando nos a 
  fazer um *pull*, depois desse pull, notaremos que  receberemos uma mensagem indicando onde se
  encontra os conflitos, e então, devemos decidir qual se manterá, simplesmente excluindo ou alterando
  esse trecho. Após isso, podemos commitar e enviar normalmente.
##

### Comandos úteis no Dia a Dia (Branches)  
- `git fetch`: Supondo que queria baixar as alterações do repositório remoto sem mesclar com o local
  essa é a exata função do git fetch.  
- `git diff`: Feito para ver as diferenças entre as branches, como exemplo `git diff main origin/main`, apresenta
  apresenta a diferença entre a main local e a main remota.  
- `git clone URL --branch 'branchName' --single-branch`: Utilizado para clonara aoenas uma branch de um devido 
  repositório.
- `git stash`: arquiva as alterações feitas anteriormente, junto ao atrubuto `list`, será listada as alterações feitas, 
  caso queria trazer de volta a nossa branch essas alterações, usamos  `git stash pop`. Em casos de salvar essas alterações 
  para usos posteriores `git stash apply`.
##  

## Dicas

- [Repositório Git Hub](https://github.com/elidianaandrade/dio-curso-git-github)
- [Myoctocat](myoctocat.com)