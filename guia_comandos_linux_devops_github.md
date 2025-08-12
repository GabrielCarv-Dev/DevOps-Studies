# Guia de Comandos Linux - Foco DevOps

Este documento reúne anotações de linha de comando e referências essenciais para uso pessoal e aprendizado de DevOps.

---

## 1. Informações de disco e arquivos
```
df -h
```
Mostra uso de espaço em disco em formato legível.

```
du -sh /caminho
```
Mostra o tamanho total de uma pasta.

```
ls -lha
```
Lista arquivos/diretórios com detalhes, tamanhos legíveis e arquivos ocultos.

```
ls -latr
```
Lista arquivos/diretórios ordenados por data (mais antigos primeiro).

---

## 2. Navegação
```
cd -
```
Volta para o último diretório.

```
pwd
```
Mostra o diretório atual.

```
tree
```
Mostra estrutura de pastas em formato de árvore.

---

## 3. Desligar e reiniciar
```
shutdown -h now
```
Desliga imediatamente.

```
shutdown -r now
```
Reinicia imediatamente.

```
reboot
```
Alternativa rápida para reiniciar.

---

## 4. Remoção de arquivos e diretórios
```
rm -rf /caminho
```
Remove recursivamente e sem confirmação (**perigoso**).

```
rmdir /caminho
```
Remove um diretório vazio.

---

## 5. Busca de arquivos/pastas
```
find /caminho -name "nome"
find /caminho -type d -name "nome"
find /caminho -type f -name "nome"
find /caminho -maxdepth 2 -type f -name "nome"
find /caminho -mtime -1
find /caminho -amin -1
find /caminho -cmin -1
find /caminho -size +1000k
```
Busca por nome, tipo, profundidade, tempo de modificação/acesso/criação ou tamanho.

---

## 6. Histórico de comandos
```
history
!n
```
Lista e repete comandos do histórico.

```
Ctrl+R
```
Busca reversa no histórico.

---

## 7. Filtro de texto
```
grep "palavra" arquivo.txt
cat arquivo.txt | grep "palavra"
grep -R "texto" /caminho
```
Procura por strings em arquivos e saídas de comando.

---

## 8. Permissões e usuários
```
chmod 755 arquivo
chown usuario:grupo arquivo
whoami
id
```
Gerencia permissões, dono e informações do usuário.

---

## 9. Processos e rede
```
ps aux
top
htop
netstat -tulnp
ss -tulnp
ping google.com
curl ifconfig.me
```
Monitora processos e rede.

---

## 10. Transferência de arquivos
```
scp arquivo usuario@servidor:/caminho
rsync -avz origem destino
```
Copia e sincroniza arquivos via rede.

---

## 11. Compressão e descompressão
```
tar -czvf arquivo.tar.gz /caminho
tar -xzvf arquivo.tar.gz
zip -r arquivo.zip pasta
unzip arquivo.zip
```
Compacta e descompacta arquivos.

---
