Principais comandos Git:

GIT CONFIG

git config --global user.name "FernandaSandre"
 - Configurar nome do usuário

git config --global user.email "fernandap.andre@gmail.com"
 - Configurar Email

git config --global core.editor vim
 - configurar editor

git config user.name
 - mostra qual o usuário configurado

git config user.email
 - mostra qual o email configurado

git config --list
 - mostra todas as configurações


PASTAS

mkdir Teste
 - cria uma pasta, no caso, Teste

cd Teste
 - acessa a pasta Teste

GIT INIT

git init
 - inicializar o repositório

ls -la
 - visualizar arquivos no diretório

ls 
 - visualizar pastas

cd ..
Voltar um nível no diretório

EDITOR DO TERMINAL (VIM)

vi Readme.md
 - cria um arquivo Readme.md

i
 - Tecla "i" premite Editar o texto

esc
 - Tecla Esc - Sai do Editor de texto

:wq
 - Sair e salvar


STATUS DOS ARQUIVOS NO GIT

UNTRACKED
- Arquivo acabou de ser adicionado mas não foi para o git

UNMODIFIED
- Logo depois que o arquivo é adicionado no git (ainda não foi modificado)

MODIFIED
- Arquivo que foi modificado

STAGED
- Arquivo aguardando a versão pronto para ser commitado.

=> Depois que for feito o commit, os arquivos voltam a ser UNMODIFIED


GIT STATUS

git status
 - Mostra o Status dos arquivos no git

git add
 - Adiciona o arquivo

COMMIT
git commit -m "Add adicionando um commit"
 - Cria um snapshot(versão) dos arquivos. O "-m" significa que vai passar uma mensagem no commit

=> Primeiro tem que adicionar o arquivo no git (git add) para depois dar o commit.

git commit -am "Mensagem"
 - para commitar um arquivo que já existe e que teve uma alteração, adiciona e commita direto.


GIT LOG

git log
 - ver o histórico das alterações.

git log --decorate 
 - mostra mais informações do histórico da versão

git log --author="Fernandasandre"
 - lista os commits do autor

git shortlog
 - em ordem alfabética, os autores e suas contribuições.

git shortlog -sn
 - quantidade de commits do autor

git log --graph
 -mostra as alterações de forma gráfica

HASH
 -é o código da alteração

GIT SHOW

git show hash
 - no lugar de hash adicionar a hh que se quer verificar
 - este comando mostra o que aconteceu no determinado commit

DIFF

git diff
 - Mostra as alterações no arquivo antes de fazer o commit

git diff --name-only
 - Mostra apenas o nome dos arquivos modificados.

DESFAZER ALTERAÇÕES

CHECKOUT
git checkout nomeDoArquivo
 - Desfaz as alterações no arquivo, e retorna o arquivo para como ele estava antes da edição.

GIT RESET - APÓS O ADD
git reset HEAD
 - Depois que o arquivo foi adicionado, através do git add, este comando remove o arquivo do Staging, e volta para o arquivo com as alterações, se der o git checkout após isso consegue desfazer a alteração.

APÓS O COMMIT
git reset --soft
 - mata o commit, mas o arquivo com as modificações ficam no staging prontos para serem commitados de novo

git reset --mixed
 - mata o commit, e volta o arquivo para antes do stagging

git reset --hard
 - mata o commit e tudo o que foi feito nele e depois


REPOSITÓRIO REMOTO

CHAVE SSH

Pegar Chave SSH

cat id_rsa.pub
 - exibe a chave ssh

more id_rsa.pub
 - exibe a chave ssh

LIGAR UM REPOSITORIO

git remote add origin 
 - depois de origin, colocar o endereço do repositório

git remote
 - mostra o repositório que já existe

git remote -v
 - mostra o repositório e mais informações sobre ele.

git push -u origin master
 - sobe as modificações para o repositório, da maser local para a master remota. Depois de fazer este comando, para subir novamente, é só usar o git push


SUBIR ARQUIVOS

git push origin master
 - envia o arquivo para a master remota.