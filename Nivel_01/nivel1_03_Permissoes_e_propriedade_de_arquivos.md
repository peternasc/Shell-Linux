
# 🟢 Nível 1 – Tópico 3: Permissões e Propriedade de Arquivos

---

## 🔍 1. O que são permissões?

Todo arquivo e pasta no Linux tem **regras de acesso**, chamadas **permissões**.

Essas regras determinam **quem pode ler, escrever ou executar** o conteúdo.

---

## 👥 2. Três tipos de usuários

As permissões se aplicam a três categorias:

| Categoria | Quem é |
|-----------|--------|
| **Usuário (u)** | Dono do arquivo |
| **Grupo (g)** | Grupo ao qual o arquivo pertence |
| **Outros (o)** | Todos os outros usuários |

---

## 🔐 3. Três tipos de permissões

| Permissão | Letra | Significado |
|-----------|-------|-------------|
| Leitura   | `r`   | Pode ver o conteúdo |
| Escrita   | `w`   | Pode modificar o conteúdo |
| Execução | `x`   | Pode rodar o arquivo (se for executável) |

---

## 🧾 4. Ver permissões com `ls -l`

```bash
ls -l
```

Exemplo de saída:
```
-rwxr-xr-- 1 peterson equipe  2048 abr 24 22:00 script.sh
```

### Interpretação da primeira coluna:
```
- rwx r-x r--
|  |   |   |
|  |   |   +--- Outros
|  |   +------- Grupo
|  +----------- Usuário (dono)
+-------------- Tipo: '-' (arquivo), 'd' (diretório)
```

---

## 🛠️ 5. Alterar permissões com `chmod`

`chmod` modifica as permissões de leitura, escrita e execução.

### Sintaxe simbólica:
```bash
chmod u+x script.sh
```

```bash
chmod o-rw publico.txt
```

### Sintaxe numérica:
| Número | Permissões | Significado        |
|--------|------------|--------------------|
| 7      | rwx        | leitura, escrita, execução |
| 6      | rw-        | leitura, escrita   |
| 5      | r-x        | leitura, execução  |
| 4      | r--        | leitura            |
| 0      | ---        | nenhuma permissão  |

```bash
chmod 755 programa.sh
```

---

## 👑 6. Alterar dono ou grupo com `chown`

`chown` permite mudar o **dono e/ou grupo** de um arquivo ou pasta.

### Exemplos:
```bash
chown admin relatorio.txt
```

```bash
chown usuario:grupo arquivo.txt
```

```bash
chown -R root:root /etc/meuarquivo
```

---

## 📁 7. Ver permissões de uma pasta

```bash
ls -ld nome_da_pasta
```

---

## 📝 Teste de fixação

### ❓1. O que significa a permissão `rwxr-xr--`?

---

### ❓2. Qual comando dá permissão de execução ao usuário dono do arquivo `meuscript.sh`?

---

### ❓3. Como você remove todas as permissões de outros usuários para o arquivo `secreto.txt`?

---

### ❓4. Qual comando altera o dono do arquivo `dados.txt` para o usuário `admin`?

---

### ❓5. O que significa a permissão numérica `644`?

---
