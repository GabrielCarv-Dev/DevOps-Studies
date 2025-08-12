CHECKLIST GIT BÁSICO

1) CONFIGURAÇÃO INICIAL
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git config --list

2) CRIAR REPOSITÓRIO
git init

3) ADICIONAR ARQUIVOS
git add arquivo.txt
git add .

4) FAZER COMMIT
git commit -m "Mensagem do commit"

5) VERIFICAR STATUS
git status

6) VER HISTÓRICO
git log
git log --oneline

7) CRIAR E TROCAR DE BRANCH
git branch nova-branch
git checkout nova-branch
git checkout -b outra-branch

8) UNIR BRANCHES
git checkout main
git merge outra-branch

9) CONECTAR A REPOSITÓRIO REMOTO
git remote add origin url_do_repositorio

10) ENVIAR PARA O REMOTO
git push origin main

11) ATUALIZAR DO REMOTO
git pull origin main

12) CLONAR REPOSITÓRIO
git clone url_do_repositorio

BOAS PRÁTICAS:
- Commits pequenos e descritivos
- Usar .gitignore
- Atualizar antes de trabalhar: git pull
