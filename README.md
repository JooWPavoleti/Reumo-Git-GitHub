# DIO / Resumo Git e Github

Repositório destinado a aula do curso da DIO sobre Versionamento de códigos Git e Github, coloando em prática o que é aprendido na aula.
Aprendendo a usar as ferramentas de código do Git para criação de repositórios locais no GitHub, clonando e criando mesmo repositório remoto na máquina! Curso completo de Versionamento de códigos Git e GitHub na DIO pelo link --> [Digital Innovation One] (https://www.dio.me/)

## 📚 DOCUMENTAÇÃO
- [Documentação Oficial Git] (https://git-scm.com/docs/git/pt_BR)
- [Documentação Oficial GitHub] (https://docs.github.com/pt/codespaces)

## 💻 Resumo das Aulas

| Aulas | Resumos |
|-----------|---------|
| Gravando Alterações no Repositório Local | [Resumo] |

## 👓 📝 Códigos Aprendidos e Anotações das Aulas

-----
- Criar novo diretório – mkdir (nome da pasta)
- Entrar no diretório ou pasta criada – cd (nome da pasta/)
- Inicializar um repositório git na pasta – git init
- Mostrar status da área de trabalho ou área de preparação – git status 
- Criando arquivo vazio no terminal – touch (README.md)
- Adicionando alterações no README do repositório remoto – git add README.md
- Salvando as alterações em um “commited” – git commit –m”” (escrever o nome do commit entre as aspas)
- Exibir as alterações e criação do commit – git log (irá exigir todas as últimas alterações e gravações realizadas no commit)
-Caso quiser que existam arquivos no projeto que não quero que sejam salvos, posso adicionar ao arquivo o código .gitignore
-Caso queira adicionar vários arquivos ignorados no nosso trabalho, digitar o código – git add .

USAR DEPOIS O COMANDO DO “COMMIT” PARA SALVAR AS ALTERAÇÕES!

Caso realizei alterações indesejadas, erradas:
- Iniciei um repositório Git em uma pasta errada, com o comando “git init” e preciso remover esse versionamento dela – rm –rf .git (para remover a força todo o conteúdo Git nesse diretório) – irá retirar a Branch “main” do diretório git e irá apagar o versionamento.

Restaurar um arquivo da nossa árvore de trabalho:

- Fiz alguma alteração em algum arquivo da minha árvore de trabalho de forma errada e remover essas alterações, restaurando a última commit salva desse nosso arquivo – git restore NOME DO ARQUIVO MODIFICADO (no caso usei como exemplo o README.md)
•	ATENÇÃO AO USAR ESSE COMANDO, POIS ELE RESTAURA A ÚLTIMA ATUALIZAÇÃO SALVA EM COMMIT

Alterar a mensagem do último commit:
- Caso eu queira alterar a mensagem gravada do último commit criado – git commit – -amend –m””(escrever a nova frase para o último commit salvo)
- Outra forma de alterar a mensagem gravada no último commit salvo é abrir um editor de texto dentro do git (é uma forma mais chata kkkk) – git commit - - amend

Irá abrir o editor de texto, primeiramente tecle o “i” para escrever no editor, faça as alterações na mensagem.

Depois de alterar, clicar em “esc” depois “:” para escrever e clicar as letras “w” e “q” para sair e clicar “enter”.


Desfazer o último commit:
- Caso queira desfazer o último commit salvo e restaurar para o versionamento salvo em um commit anterior a esse último:

Reset - - soft: Comando que usamos para pegar os arquivos que estavam gravados nos commits anteriores aos indicados e colocar, adicionar de volta esses arquivos na nossa área de preparação. – git reset - - soft (colar o código último commit que deseja voltar e não desfazer).

Reset - -mixed: Comando que usamos para pegar os arquivos que estavam gravados nos commits anteriores aos indicados e colocar, adicionar de volta esses arquivos na nossa área de preparação como arquivos ignorados ou não reconhecidos, precisamos colocar novamente na nossa área de preparação – git reset - - mixed (colar o código último commit que deseja voltar e não desfazer).

Reset - -hard: A utilização desse comando irá desfazer todos os arquivos salvos nos commits anteriores ao indicado, então tomar muito cuidado para usar esse comando. – git reset - -hard (colar o código último commit que deseja voltar e não desfazer).

Se eu quiser ter um histórico mais detalhado das alterações que fiz – git reflog

- Para conectar os dois repositórios, do GitHub no da máquina – git remote add origin (COLOCAR A URL DO REPOSITÓRIO DO GITHUB).

Comando responsável por enviar as alterações do repositório local (máquina) para o repositório remoto (GitHub), ou seja, ele puxa e mescla as alterações salvas da máquina para o GitHub – git push
- Complementações do comando “git push”

-u: responsável por dizer ao git para mesclar as branches do local e remoto, ou seja,configurar e mostrar ao Git que a main “origin” do repositório remoto (GitHub) está conectada e mesclada a main do repositório local (máquina) indicando assim qual banche puxar.

-git push –u origin main

Git push: é o comando para puxar as alterações entre os repositórios

-u: configuração para dizer ao Git as branches a serem mescladas do repositório remoto e local

Origin: nome da Branche, no caso do exemplo, do repositório remoto (GitHub)

Main: nome da Branche, no caso, do repositório local (máquina)


Comando responsável para enviar as alterações realizadas no repositório remoto (GitHub) para o repositório local (máquina), ou seja, mescla as alterações realizadas do GitHub para o repositório da máquina – git pull


- Para criar uma branch nova dentro da branch atual

Para trocar da branch atual a branch nova criada dentro da atual – git checkout –b (COLOCAR O NOME A SER DADO A NOVA BRANCH, NO CASO DA AULA SERÁ O NOME “TESTE”).

Para trocar da branch nova criada para a branch original – git checkout (NOME DA BRANCH ORIGINAL, NO CASO DA AULA É MainJooW).

- PODE SER OBSERVADO ASSIM QUE, O ARQUIVO CRIADO ENQUANTO UTILIZÁVAMOS A BRANCH CRIADA “TESTE” NÃO APARECEM QUANDO VOLTAMOS PARA A BRANCH ORIGINAL “MainJooW”, ISSO PORQUE AS ALTERAÇÕES NAS BRANCHES CRIADAS SÃO RAMIFICAÇÕES INDEPENDENTES DO PROJETO ORIGINALMENTE CRIADO!

Para abrir na tela a lista dos últimos commit criadas em cada Brach – git branch –v

- Para mesclar as Branches:

Para que todas as alterações e arquivos criados em Branches diferentes, preciso mesclar elas através do comando – git merge (COLOCAR O NOME DA BRANCH QUE DESEJAMOS MESCLAR A ORIGINAL, NO CASO DA AULA É O NOME “TESTE”)

Para listar as Branches que temos criadas nesse repositório – git branch

Para excluir a Branch que não precisa mais – git branch –d (NOME DA BRANCH QUE DESEJAMOS EXCLUIR, NO CASO DA AULA É O NOME “TESTE”)

- Tratando Alterações entre Branches local e Remoto:
 
Para baixar as alterações do repositório remoto para o git do repositório local, mas sem mesclar essas alterações – git fetch origin MainJooW (onde “origin” é o nome do repositório remoto para baixar na nossa branch “MainJooW)

Para mesclar essas alterações no repositório local, depois te traze-las com o “fetch” usamos o comando – git merge origin/MainJooW

Caso queira clonar um repositório com várias branches, mas quer clonar apenas uma das branches do repositório – git clone (COLAR A URL DO REPOSITÓRIO REMOTO) - - branch teste - -single-branch

Se por algum motivo, estando nessa branch clonada no repositório local, acabar fazendo alguma alteração e precisar criar uma nova Branch mas não quero que esta alteração vá junto nessa nova branch, existe um comando para que eu possa arquivar essa alteração – git stash

Posso ver uma lista das alterações arquivadas pelo comando – git stash list

Dessa forma posso abrir uma nova branch e trabalhar nela, sem ter as alterações realizadas na branch anterior.

Caso queria voltar as modificações realizadas na banch e apagar essa alteração da lista arquivada com “stash” – git stash pop

Caso queira voltar as modificações realizadas na branch mas desejo continuar com ela na lista de arquivamento da “stash” – git stash apply



- README – é o lugar no repositório local, onde irei colocar tudo que compõe meu projeto, a descrição, o que representa, imagens, diagramas, tudo que existe e que seja importante do projeto, todo histórico.
- MARKDOWN – Forma de linguagem de marcação simples, tipo URLL, editando textos, etc.
--------
