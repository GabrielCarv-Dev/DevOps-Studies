# Guia de Comandos Linux - Foco DevOps

Este repositório serve como referência pessoal para comandos Linux úteis, especialmente para uso em DevOps.  
Inclui exemplos, explicações e boas práticas.

---

## 1. Informações de disco e arquivos
```bash
df -h
```
Mostra uso de espaço em disco em formato legível.

```bash
du -sh /caminho
```
Mostra tamanho total de uma pasta.

```bash
ls -lha
```
Lista arquivos/diretórios com detalhes, tamanhos legíveis e arquivos ocultos.

```bash
ls -latr
```
Lista ordenado por data (mais antigos primeiro).

---

## 2. Navegação
```bash
cd -
```
Volta para o último diretório.

```bash
pwd
```
Mostra o diretório atual.

```bash
tree
```
Mostra estrutura de pastas em árvore.

---

## 3. Desligar e reiniciar
```bash
shutdown -h now
```
Desliga imediatamente.

```bash
shutdown -r now
```
Reinicia imediatamente.

```bash
reboot
```
Alternativa para reiniciar.

---

## 4. Remoção de arquivos e diretórios
```bash
rm -rf
```
Remove recursivamente e sem confirmação (**perigoso**).

```bash
rmdir /caminho
```
Remove um diretório vazio.

---

## 5. Busca de arquivos/pastas
```bash
find /caminho -name "nome"
find /caminho -type d -name "nome"
find /caminho -type f -name "nome"
find /caminho -maxdepth 2 -type f -name "nome"
find /caminho -mtime -1
find /caminho -amin -1
find /caminho -cmin -1
find /caminho -size +1000k
```
Busca por nome, tipo, tempo de modificação/acesso/criação ou tamanho.

---

## 6. Histórico de comandos
```bash
history
!n
```
Lista e repete comandos do histórico.

```bash
Ctrl+R
```
Busca reversa no histórico.

---

## 7. Filtro de texto
```bash
grep "palavra" arquivo.txt
cat arquivo.txt | grep "palavra"
grep -R "texto" /caminho
```
Procura por strings em arquivos e saídas de comando.

---

## 8. Permissões e usuários
```bash
chmod 755 arquivo
chown usuario:grupo arquivo
whoami
id
```
Gerencia permissões, dono e informações do usuário.

---

## 9. Processos e rede
```bash
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
```bash
scp arquivo usuario@servidor:/caminho
rsync -avz origem destino
```
Copia e sincroniza arquivos via rede.

---

## 11. Compressão e descompressão
```bash
tar -czvf arquivo.tar.gz /caminho
tar -xzvf arquivo.tar.gz
zip -r arquivo.zip pasta
unzip arquivo.zip
```
Compacta e descompacta arquivos.

---

## Observação
Esta lista cobre a maioria das situações básicas que um DevOps iniciante pode encontrar.
