# Resumos Bootcamp Dio
  
Repositório reservado para armazenar resumos dos tópicos do Bootcamp da Dio
FullStack Java + Angular [Digital Innovation One](https://www.dio.me/)

##
  
## 📕 Documentação

- [Documentação Git](https://git-scm.com/doc)
- [Documentação Github](https://docs.github.com/)
- [Documentação JavaScript](https://262.ecma-international.org/5.1/)
- [Documentação Java](https://docs.oracle.com/en/java/)
- [Documentação AngularJs](https://angular.io/docs)
  
## 💻 Resumos

| Aulas | Resumos |
|-------|---------|

##
  
### Commitando arquivos

```
- git init
- git add filename
- git commit -m "first commit"

```
  
### Restaurando arquivos

É normal excluirmos ou editarmos algum arquivo de maneira indesejada as vezes, e acabarmos salvando sem querer... Ao invés de pensarmos que todo o progresso está perdido. Ainda tem uma forma de retornar a edição anterior do arquivo:

```
- git restore filename.extension
```
  
**Importante notar que ao executar esse comando, deve ter certeza que não precisará de nehum alteração feita no arquivo**
  
### Alterando mensagem do último commit

```
- git commit --amend -m "new message"
```
  
>Caso escreva o código acima sem o "-m". Resultará em algo desse tipo:

`- git commit --amend`
  
```
first commit //Press i for edit commit name

# PLease enter the commit message for your changes. Lines starting
# with '#' will ignored, and an empty message aborts the commit.
#
# Date:     Day Month XX HH:MIN:SEC YEAR _XXXX
#
# On branch branchName
# Changes to be commited
#           new file: .gitignore
#           new file: filename.ext
#
//To exit press 'Esc' an window input will be open, type ':wq'
```
  
### Retornando a um commit anterior
  
Supondo que você queira não alterar simplesmente um nome de commit, e sim
retornar a esse commit anterior. Para isso podemos usar o 'git reset'
acompanhado dos parametros `--soft`, `--mixt` ou `--hard`.
  
- A propriedade `--soft`, funciona de forma que através do `git log`, você
  acesse o hash do commit desejado, e com esse hash, retorne até o próprio.
    `git reset --soft 4dwe322e3HASHHERE82398dadq`
&nbsp;
- Já à `--mixt`, é o comportamento padrão do git reset, ele pega seus arquivos
  posteriores ao hash indicado e coloca na commit área.
    `git reset --mixt hashNumber` ou `git reset hashNumber`
&nbsp;
- E por último à `--hard`, reseta completamente todos os comits posteriores e exclui
  os arquivos deixando apenas os dos arquivos do commit desejado.
    `git reset --hard hashNumber`
  
>Além disso o git tambem permite remover arquivos específicos das áreas de preparação
usando o `git reset folder/archive`, assim esse arquivo em específico será removido
da commit área, para desfazer o precedimento o próprio git já indica o uso do
`git restore --staged folder/archive`.
