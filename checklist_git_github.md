
# Checklist e Snippets — Atualizar arquivos no Git/GitHub

## 📌 Fluxo rápido (sem mudanças remotas)
```bash
# 0) Conferir em qual branch está
git branch

# 1) Ver o que mudou
git status

# 2) Adicionar mudanças (arquivo específico ou tudo)
git add NOME_ARQUIVO
# ou
git add .

# 3) Commit (mensagem curta, verbo no imperativo)
git commit -m "Atualiza NOME_ARQUIVO com X"

# 4) Enviar
git push origin main   # Troque 'main' se seu branch tiver outro nome
```

---

## 📌 Se houve mudanças no remoto (GitHub) antes
```bash
# 1) Trazer as mudanças
git pull --ff-only origin main   # Falha se exigir merge; evita commits "merge" acidentais

# (Se falhar com --ff-only, use:)
git pull --rebase origin main    # Reescreve sua sequência por cima do remoto (histórico limpo)

# 2) Agora faça seu fluxo normal
git add .
git commit -m "Descrição objetiva do que mudou"
git push origin main
```

---

## 📌 Resolver conflitos
```bash
# 1) O Git vai marcar os arquivos conflitados
git status

# 2) Abra os arquivos e resolva os trechos marcados por:
# <<<<<<< HEAD
# =======
# >>>>>>> <commit-remoto>

# 3) Depois de resolver:
git add ARQUIVO_CONFLITADO

# 4) Continue o rebase (se estava em rebase) ou finalize o merge
git rebase --continue   # Se você usou pull --rebase
# ou
git commit              # Se estava em merge e faltou o commit de merge

# 5) Envie
git push origin main
```

---

## 📌 Checagens úteis
```bash
git log --oneline --graph --decorate -n 10   # Histórico curto e visual
git diff                                     # Ver diferenças não adicionadas
git diff --staged                            # Ver o que vai no commit
git remote -v                                # Conferir URL do remoto (HTTPS/SSH)
```

---

## 📌 Boas práticas de mensagens
- Primeira linha **≤ 50 caracteres**, verbo no imperativo:
  - `feat: adiciona validação de CEP`
  - `fix: corrige cálculo de frete`
- Detalhes (se necessário) em parágrafos abaixo da primeira linha.
- Evite `update`, `ajustes`, `fixes` genéricos.

---

## 📌 Snippet rápido com placeholders
```bash
# Atualizar sem mudanças remotas
git add {{NOME_ARQUIVO}}      # ou git add .
git commit -m "{{Descrição curta do que foi alterado}}"
git push origin {{NOME_DO_BRANCH}}

# Atualizar com mudanças remotas
git pull --ff-only origin {{NOME_DO_BRANCH}} || git pull --rebase origin {{NOME_DO_BRANCH}}
git add {{NOME_ARQUIVO}}      # ou git add .
git commit -m "{{Descrição curta do que foi alterado}}"
git push origin {{NOME_DO_BRANCH}}

# Resolver conflitos
git status
# editar arquivos e remover <<<<<<< ======= >>>>>>> 
git add {{ARQUIVO_CONFLITADO}}
git rebase --continue  # ou git commit
git push origin {{NOME_DO_BRANCH}}
```
