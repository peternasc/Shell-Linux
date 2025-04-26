
# 🟢 Nível 1 – Tópico 2: Criação e Manipulação de Arquivos e Pastas

---

## 🧾 1. `touch` – Criar arquivos vazios

O comando `touch` é usado para:

- Criar arquivos **vazios**
- Atualizar a **data de modificação** de arquivos existentes

> É ideal para **iniciar novos arquivos** que serão preenchidos depois.

### Exemplos:
```bash
touch lista.txt
```

```bash
touch arquivo1.txt arquivo2.txt
```

```bash
touch pasta/relatorio.txt
```

---

## 📂 2. `mkdir` – Criar diretórios

O comando `mkdir` cria **novas pastas** (diretórios).

> Use-o para organizar seus arquivos em estruturas lógicas.

### Exemplos:
```bash
mkdir projetos
```

```bash
mkdir projetos/scripts
```

```bash
mkdir -p projetos/bash/testes
```

---

## 🔄 3. `mv` – Mover ou renomear arquivos e pastas

O comando `mv` pode ser usado de duas formas:

- **Mover** arquivos ou pastas de um lugar para outro
- **Renomear** arquivos ou pastas

### Exemplos:
```bash
mv texto.txt documentos/
```

```bash
mv antigo.txt novo.txt
```

```bash
mv *.txt textos/
```

---

## 📄 4. `cp` – Copiar arquivos e pastas

O comando `cp` é usado para criar **cópias** de arquivos e pastas.

> Para **copiar pastas inteiras**, é necessário usar a opção `-r`.

### Exemplos:
```bash
cp arquivo.txt copia.txt
```

```bash
cp -r projeto projeto_backup
```

---

## 🗑️ 5. `rm` – Remover arquivos e pastas

O comando `rm` apaga **arquivos ou pastas** do sistema.

> ⚠️ Não há lixeira! O conteúdo é **apagado permanentemente**.

### Exemplos:
```bash
rm arquivo.txt
```

```bash
rm -r pasta_antiga/
```

```bash
rm -rf *
```

---

## 🧠 6. Resumo dos comandos

| Comando | Função básica                      | Opções úteis     |
|--------|-------------------------------------|------------------|
| `touch` | Cria arquivos vazios               | —                |
| `mkdir` | Cria pastas                        | `-p` para criar hierarquia |
| `mv`    | Move ou renomeia arquivos/pastas   | —                |
| `cp`    | Copia arquivos e pastas            | `-r` para copiar pastas |
| `rm`    | Remove arquivos/pastas             | `-r`, `-f`       |

---

## 📝 Teste de fixação

### ❓1. Para que serve o comando `touch`?

---

### ❓2. Como criar uma estrutura de pastas `projetos/bash/testes`?

---

### ❓3. Qual comando copia o arquivo `relatorio.txt` para dentro da pasta `documentos`?

---

### ❓4. O que o comando `rm -rf /meus_arquivos` faz? Por que é perigoso?

---

### ❓5. Como renomear `rascunho.txt` para `versao_final.txt`?

---
