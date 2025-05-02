
# 🟠 Nível 3 – Tópico 9: Testes de Arquivos — `-f`, `-d`, `-e` e outros

---

## 📖 1. O que são testes de arquivos?

Os **testes de arquivos** permitem que um script verifique:

- **Se o arquivo ou diretório existe**
- **Qual é o tipo** (arquivo, diretório, link, etc)
- **Se é possível ler, gravar ou executar**

Esses testes ajudam a **prevenir erros e garantir que o script só trabalhe com arquivos válidos**.

---

## 📚 2. Principais operadores de teste de arquivos

| Operador | Significado |
|:---|:---|
| `-e` | Verifica se o arquivo **existe** |
| `-f` | Verifica se é um **arquivo regular** |
| `-d` | Verifica se é um **diretório** |
| `-r` | Verifica se é **legível** (permite leitura) |
| `-w` | Verifica se é **gravável** (permite escrita) |
| `-x` | Verifica se é **executável** |
| `-s` | Verifica se o arquivo **não está vazio** |

---

## 🛠️ 3. Exemplos práticos

### 📌 Verificar se o arquivo existe:

```bash
if [ -e arquivo.txt ]
then
    echo "O arquivo existe."
else
    echo "O arquivo não existe."
fi
```

---

### 📌 Verificar se é um arquivo regular:

```bash
if [ -f arquivo.txt ]
then
    echo "É um arquivo normal."
fi
```

---

### 📌 Verificar se é um diretório:

```bash
if [ -d pasta ]
then
    echo "É um diretório."
fi
```

---

### 📌 Verificar permissões:

```bash
if [ -r arquivo.txt ]
then
    echo "Arquivo é legível."
fi

if [ -w arquivo.txt ]
then
    echo "Arquivo é gravável."
fi

if [ -x script.sh ]
then
    echo "Arquivo é executável."
fi
```

---

### 📌 Verificar se o arquivo NÃO está vazio:

```bash
if [ -s arquivo.txt ]
then
    echo "Arquivo não está vazio."
else
    echo "Arquivo está vazio."
fi
```

---

## 🧠 4. Usando com parâmetros

Você pode usar junto com variáveis:

```bash
arquivo="meuarquivo.txt"

if [ -e "$arquivo" ]
then
    echo "O arquivo $arquivo existe."
fi
```

---

## 🎯 Boas práticas

- Sempre coloque variáveis **entre aspas** (`"$arquivo"`) para evitar problemas com espaços.
- Combine testes para validações mais robustas (exemplo: verificar se o arquivo existe **e** é gravável).
- Use esses testes sempre que o script for manipular arquivos para evitar falhas inesperadas.

---
