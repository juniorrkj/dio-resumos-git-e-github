# 📌 Trabalhando com Branches no Git

## 🔹 Criando uma Branch
Criar uma nova branch:  
git branch nome-da-branch  

Criar e mudar para a nova branch imediatamente:  
git checkout -b nome-da-branch  

Ver todas as branches disponíveis:  
git branch  

Ver todas as branches remotas:  
git branch -r  

Ver todas as branches locais e remotas:  
git branch -a  

---

## 🔹 Trocando de Branch
Mudar para outra branch existente:  
git checkout nome-da-branch  

A partir do Git 2.23+, pode-se usar:  
git switch nome-da-branch  

Voltar para a branch principal (`main` ou `master`):  
git checkout main  
# ou  
git switch main  

Retornar para a última branch utilizada:  
git checkout -  

---

## 🔹 Trabalhando com Branches Remotas
Criar uma branch e enviá-la para o repositório remoto:  
git push -u origin nome-da-branch  

Baixar todas as branches remotas para sua máquina:  
git fetch --all  

Atualizar a branch local com mudanças do repositório remoto:  
git pull origin nome-da-branch  

Baixar uma branch remota para sua máquina:  
git checkout -b nome-da-branch origin/nome-da-branch  

---

## 🔹 Mesclando (Merge) Branches
Para juntar as alterações de uma branch na `main`:  
1. Vá para a branch principal:  
   git checkout main  

2. Atualize sua branch antes do merge:  
   git pull origin main  

3. Faça o merge da outra branch:  
   git merge nome-da-branch  

Se houver conflitos, resolva-os manualmente, adicione os arquivos corrigidos e finalize o merge:  
git add .  
git commit -m "Resolvendo conflitos de merge"  

---

## 🔹 Rebase (Alternativa ao Merge)
Rebase permite trazer mudanças de outra branch de uma forma mais limpa:  
git rebase nome-da-branch  

Se houver conflitos durante o rebase, resolva manualmente e continue com:  
git rebase --continue  

Se precisar cancelar o rebase:  
git rebase --abort  

---

## 🔹 Deletando Branches
Deletar uma branch **local**:  
git branch -d nome-da-branch  

Se a branch ainda não foi mesclada, use `-D` para forçar a exclusão:  
git branch -D nome-da-branch  

Deletar uma branch **remota**:  
git push origin --delete nome-da-branch  

---

## 🔹 Comandos Úteis no Dia a Dia
Verificar em qual branch você está:  
git branch --show-current  

Verificar o histórico de branches e merges:  
git log --oneline --graph --all  

Verificar quais branches já foram mescladas na `main`:  
git branch --merged main  

Verificar quais branches **não foram** mescladas na `main`:  
git branch --no-merged main  

Renomear uma branch **localmente**:  
git branch -m antigo-nome novo-nome  

Renomear uma branch **remota** (exclui e cria novamente):  
git push origin --delete antigo-nome  
git push -u origin novo-nome  

Forçar a sincronização de todas as branches locais com as remotas (cuidado ao usar):  
git fetch --prune  

---
