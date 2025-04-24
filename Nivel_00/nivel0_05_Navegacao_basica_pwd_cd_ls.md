
# 🟤 Nível 0 – Tópico 3: Navegação básica: `pwd`, `cd`, `ls`

---

## 📂 1. Por que aprender navegação?

Saber **se mover entre diretórios** e visualizar arquivos é essencial para qualquer atividade em Linux.  
Esses três comandos (`pwd`, `cd`, `ls`) são a base de tudo que você vai fazer no terminal.

---

## 🔍 2. `pwd` – Onde estou?

`pwd` vem de **"Print Working Directory"**.  
Ele mostra o **diretório atual** em que você está.

### Exemplo:
```bash
pwd
```

Saída:
```
/home/peterson
```

---

## 🧭 3. `cd` – Mover-se entre pastas

`cd` significa **"Change Directory"**.  
Com ele, você entra ou sai de pastas no sistema.

### Exemplos:
```bash
cd /etc         # Vai direto para o diretório /etc
cd ..           # Volta um nível acima
cd              # Volta para sua pasta pessoal (home)
cd /var/log     # Entra na pasta de logs do sistema
```

### Dica:
Use `Tab` para completar automaticamente o nome da pasta.

---

## 📋 4. `ls` – Listar arquivos e pastas

`ls` mostra o conteúdo do diretório atual.

### Exemplos:
```bash
ls              # Lista arquivos e pastas simples
ls -l           # Lista com detalhes (permissões, tamanho, data)
ls -a           # Mostra arquivos ocultos (os que começam com .)
ls -lh          # Lista com tamanhos legíveis (K, M, G)
```

### Saída típica de `ls -l`:
```
-rw-r--r--  1 peterson peterson  4096 abr 23 14:10 arquivo.txt
```

| Parte        | Significado                        |
|--------------|------------------------------------|
| `-rw-r--r--` | Permissões                         |
| `1`          | Número de links                    |
| `peterson`   | Dono do arquivo                    |
| `4096`       | Tamanho em bytes                   |
| `abr 23 14:10`| Data de modificação               |
| `arquivo.txt`| Nome do arquivo                    |

---

## 📌 5. Navegação combinada

```bash
cd /var/log
ls -lh
cd ..
pwd
```

Esse exemplo:
1. Entra em `/var/log`
2. Lista arquivos com detalhes
3. Volta um nível acima
4. Mostra o caminho atual

---

## 📝 Teste de fixação

Responda com base no conteúdo acima:

### ❓1. Qual comando mostra o caminho da pasta atual?

---

### ❓2. O que o comando `cd ..` faz?

---

### ❓3. Qual a diferença entre `ls` e `ls -lh`?

---

### ❓4. Como ver arquivos ocultos com o comando `ls`?

---

### ❓5. O que o comando `cd` sem argumentos faz?

---

Pronto! Agora que você já sabe navegar, no próximo tópico vamos entender como **criar, mover, copiar e apagar arquivos e diretórios no terminal**!
