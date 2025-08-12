
Git - Comandos e Boas Práticas
=============================================

Fluxo rápido (sem mudanças remotas)
------------------------------------
1. Conferir em qual branch está:
   git branch

2. Ver o que mudou:
   git status

3. Adicionar mudanças (arquivo específico ou tudo):
   git add NOME_ARQUIVO
   git add .

4. Commit (mensagem curta, verbo no imperativo):
   git commit -m "Mensagem"

5. Enviar para o GitHub:
   git push origin main

Fluxo com mudanças remotas no GitHub
-------------------------------------
1. Trazer as mudanças:
   git pull --ff-only origin main

2. Se o comando acima falhar, usar:
   git pull --rebase origin main

3. Adicionar mudanças:
   git add .

4. Commit:
   git commit -m "Mensagem"

5. Enviar para o GitHub:
   git push origin main

Resolução de conflitos
-----------------------
1. O Git marca os arquivos com conflito:
   git status

2. Editar os arquivos e resolver as seções:

3. Marcar como resolvido:
   git add ARQUIVO_CONFLITADO

4. Continuar o rebase (se aplicável):
   git rebase --continue

5. Ou finalizar o merge:
   git commit

6. Enviar para o GitHub:
   git push origin main

Comandos úteis
--------------
- Ver histórico curto:
  git log --oneline --graph --decorate -n 10

- Ver diferenças não adicionadas:
  git diff

- Ver diferenças que irão para o commit:
  git diff --staged

- Conferir remoto configurado:
  git remote -v

Boas práticas de mensagens de commit
------------------------------------
- Primeira linha com até 50 caracteres, verbo no imperativo:
  Exemplo: feat: adiciona validação de CEP
  Exemplo: fix: corrige cálculo de frete

- Se necessário, adicionar mais detalhes em parágrafo abaixo.

- Evitar mensagens genéricas como "update", "ajustes", "fixes".

- Usar prefixos quando possível (conventional commits):
  feat: nova funcionalidade
  fix: correção de bug
  docs: alteração na documentação
  style: mudanças visuais ou formatação
  refactor: refatoração de código
  test: adição ou ajuste de testes
  chore: tarefas internas ou manutenção
