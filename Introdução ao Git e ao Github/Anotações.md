
# 1. O que é git e github?


Git é um sistema de versionamento de arquivos.

Github é uma plataforma de armazenamento de versões git.


## 1.1 Conceitos importantes


Respositórios são "pastas" do git, utilizadas para armazenamento de projetos
Branch é uma ramificação a partir de um fluxo principal
Commit são alterações feitas no projeto
Merge é a junção de uma branch alternativa com uma branch principal
Push é trazer os arquivos para o repositório remoto
Pull request são contribuições feitas em projetos OpenSource

# 2. Utilizando o Git e Github

Antes de utilizarmos o git é necessário configurá-lo com nome e o e-mail do usuário:



$ git config --global user.name "nome do usuário"
$ git config --global user.email "emaildousuario@exemplo.com"


Para verificar se as configurações foram feitas utilize o seguinte parâmetro:



$ git config --list


Ao inciar um novo repositório colocamos no Git Bash:



$ git init


Criado nosso repositório, devemos passar todos os arquivos desejados para área de stagging:



$ git add .


Ao colocar o ., estamos adicionando todos os arquivos presentes na nossa pasta, para adicionar um único item utilize o parâmetro:



$ git add nomeDoAqruivo.txt


Chegou a hora de commitar nosso arquivo. Para isso digite:



$ git commit -m "primeiro commit"


Entre aspas, é indicado que se coloque o nome da alteração feita no arquivo afim de facilitar a identificação dessas alterações.

O git bash, por padrão vem com a branch master, caso seja necessário modificar a branch principal para main, por exemplo, basta colocar:



$ git branch -M "main"


Chegou a hora de passar nossos arquivos para o Github. Na git bash digite:



$ git remote add origin link-do-github.com


O remote irá fazer a conexão entre o repositório da máquina e o github. Em seguida, utilizamos o push para poder "empurrar" nosso repositório para o github:



$ git push -u origin main


Na primeira vez que fizermos o push para o github, aparecerá uma tela de login e em seguida uma tela de autorização no browser, clique no botão de autorização verde e confirme sua senha. Feito isso, a primeira versão do seu arquivo estará no github.

Caso deseje adicionar uma nova versão do seu arquivo ou arquivos novos, basta voltar repetir os comandos de add, commit e push.

Ah! Também é possível visualizar o status do seu repositório, os aquivos que sofreram modificações e se eles foram commitados corretamente, basta colocar:



$ git status


E caso queira excluir algum arquivo do github, coloque:



$ git rm nomeDoArquivo.txt


Após utilizar o comando de exclusão, repita os comandos de commit e push.
