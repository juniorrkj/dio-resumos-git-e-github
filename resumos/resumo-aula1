GIT BASICO

📌 Configuração Inicial
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
git config --global core.editor "vim"  # Define o editor padrão
git config --list  # Exibe as configurações atuais

📌 Criar e Clonar Repositório
git init  # Inicializa um repositório Git local
git clone URL_DO_REPOSITORIO  # Clona um repositório remoto

📌 Adicionar e Confirmar Alterações
git status  # Mostra o status dos arquivos no repositório
git add arquivo.txt  # Adiciona um arquivo específico à área de stage
git add .  # Adiciona todos os arquivos modificados
git commit -m "Mensagem do commit"  # Confirma as mudanças
git commit --amend -m "Nova mensagem"  # Modifica o último commit

📌 Visualizar Histórico
git log  # Exibe o histórico de commits
git log --oneline --graph --all  # Histórico simplificado com branch
git show ID_DO_COMMIT  # Mostra detalhes de um commit específico


📌 Trabalhando com Branches
git branch  # Lista as branches no repositório
git branch nova-branch  # Cria uma nova branch
git checkout nova-branch  # Troca para a branch desejada
git checkout -b nova-branch  # Cria e muda para a nova branch
git branch -d nome-da-branch  # Exclui uma branch local
git push origin --delete nome-da-branch  # Exclui uma branch remota

📌 Sincronizar com Repositório Remoto
git remote -v  # Lista os repositórios remotos
git remote add origin URL_DO_REPOSITORIO  # Adiciona um repositório remoto
git fetch origin  # Busca as mudanças do repositório remoto
git pull origin main  # Atualiza o repositório local com o remoto
git push origin main  # Envia commits para o repositório remoto


📌 Reverter Alterações
git checkout -- arquivo.txt  # Descarta alterações não adicionadas ao stage
git reset HEAD arquivo.txt  # Remove do stage, mas mantém a modificação
git reset --hard HEAD  # Desfaz todas as mudanças desde o último commit
git revert ID_DO_COMMIT  # Cria um commit revertendo as mudanças de um commit específico

📌 Stash (Guardar Alterações Temporariamente)
git stash  # Salva as alterações pendentes sem fazer commit
git stash list  # Lista os stashes salvos
git stash apply  # Aplica o último stash salvo
git stash drop  # Remove um stash
git stash pop  # Aplica e remove o stash

📌 Tags (Marcação de Versões)
git tag v1.0  # Cria uma tag chamada v1.0
git tag  # Lista todas as tags
git show v1.0  # Mostra detalhes da tag
git push origin v1.0  # Envia a tag para o repositório remoto

📌 Criar um .gitignore
touch .gitignore  # Cria o arquivo
nano .gitignore   # Edita o arquivo no terminal

📌 Exemplos de regras no .gitignore
# Ignorar arquivos de log e temporários
*.log
*.tmp

# Ignorar pastas específicas
node_modules/
dist/
build/
venv/

# Ignorar arquivos de credenciais
.env
secrets.json

# Ignorar tudo em uma pasta, exceto um arquivo específico
data/*
!data/importante.txt

📌 Ver arquivos ignorados
git status --ignored  # Lista arquivos ignorados pelo `.gitignore`

📌 Como usar .gitkeep para manter uma pasta vazia
1 Crie a pasta vazia

bash
Copiar
Editar
mkdir minha-pasta-vazia
2️ Crie um arquivo .gitkeep dentro dela

bash
Copiar
Editar
touch minha-pasta-vazia/.gitkeep
3️ Adicione e faça commit

bash
Copiar
Editar
git add minha-pasta-vazia/.gitkeep
git commit -m "Mantendo a pasta minha-pasta-vazia no repositório"
git push origin main
📌 Por que usar .gitkeep?
🔹 O Git não rastreia pastas vazias, então .gitkeep serve como um "marcador" para garantir que a pasta seja mantida.
🔹 Isso é útil para diretórios que devem existir no projeto, mas que podem começar vazios, como logs/, uploads/, temp/, etc.

Obs: O nome .gitkeep não é um padrão oficial do Git, mas uma convenção usada por desenvolvedores. Você pode nomear o arquivo de outra forma se quiser.

GIT AVANÇADO

📌 Manipulação Avançada de Histórico
git rebase branch-alvo  # Reaplica commits em cima de outra branch
git rebase -i HEAD~3  # Rebase interativo para editar os últimos 3 commits
git rebase --abort  # Cancela um rebase em andamento
git rebase --continue  # Continua um rebase após resolver conflitos

📌 Aplicar Commits Específicos
git cherry-pick ID_DO_COMMIT  # Aplica um commit específico de outra branch
git cherry-pick ID1 ID2  # Aplica múltiplos commits específicos
git cherry-pick -n ID_DO_COMMIT  # Aplica o commit sem confirmar (commit pendente)

📌 Depuração e Localização de Problemas
git bisect start  # Inicia o processo de busca binária de bugs
git bisect bad  # Marca a versão atual como ruim (com bug)
git bisect good ID_DO_COMMIT  # Marca um commit antigo como bom (sem bug)
git bisect reset  # Encerra o bisect e volta ao estado normal

📌 Trabalhando com Hooks (Automação no Git)
cd .git/hooks  # Acessa a pasta de hooks do Git
touch pre-commit  # Cria um hook que executa antes de cada commit
chmod +x pre-commit  # Dá permissão de execução ao script
nano pre-commit  # Edita o hook para adicionar scripts personalizados

📌 Outros Comandos Avançados
git reflog  # Mostra o histórico de todas as ações feitas no repositório
git blame arquivo.txt  # Mostra quem alterou cada linha de um arquivo e quando
git shortlog -sn  # Lista os contribuidores e a quantidade de commits de cada um
git grep "palavra"  # Busca um termo dentro dos arquivos versionados pelo Git
