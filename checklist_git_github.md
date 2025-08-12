
# Atualizar sem mudanças remotas
# 0) conferir branch atual
git branch

# 1) ver mudanças
git status

# 2) adicionar alterações
git add {{NOME_ARQUIVO}}      # arquivo específico
# ou tudo
git add .

# 3) commit (mensagem clara, verbo no imperativo)
git commit -m "{{Descrição curta do que foi alterado}}"

# 4) enviar para o GitHub
git push origin {{NOME_DO_BRANCH}}   # ex.: main

------------------------------------------------------------

# Atualizar com mudanças remotas antes

# 1) trazer mudanças remotas sem merge automático
git pull --ff-only origin {{NOME_DO_BRANCH}}

# (se falhar, usar rebase para manter histórico limpo)
git pull --rebase origin {{NOME_DO_BRANCH}}

# 2) adicionar mudanças
git add {{NOME_ARQUIVO}}
# ou tudo
git add .

# 3) commit
git commit -m "{{Descrição curta do que foi alterado}}"

# 4) enviar
git push origin {{NOME_DO_BRANCH}}

---------------------------------------------------------------

# Resolver conflitos

# listar conflitos
git status

# editar arquivos e remover marcadores:
# <<<<<<< HEAD
# =======
# >>>>>>> {{ID_DO_COMMIT_REMOTO}}

# marcar como resolvido
git add {{ARQUIVO_CONFLITADO}}

# se estava em rebase:
git rebase --continue

# se estava em merge:
git commit

# enviar
git push origin {{NOME_DO_BRANCH}}

-----------------------------------------------------------------

# Consultas rápidas

git log --oneline --graph --decorate -n 10   # histórico curto
git diff                                     # ver alterações não adicionadas
git diff --staged                            # ver o que vai no commit
git remote -v                                # ver remoto configurado
