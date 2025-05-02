
# 🟠 Nível 3 – Tópico 8: Leitura de Arquivos Linha a Linha com `while read`

---

## 📖 1. Para que serve o `while read`?

O `while read` é uma técnica no Bash para:

- **Ler arquivos linha por linha**
- Processar dados de forma organizada e controlada
- Fazer loops sob demanda, onde cada iteração é uma linha do arquivo

É extremamente útil para:

- Processar listas
- Ler arquivos de configuração
- Automatizar tarefas com entrada de dados

---

## 📚 2. Sintaxe básica

```bash
while read linha
do
    comandos usando $linha
done < arquivo.txt
```

| Componente | Significado |
|:---|:---|
| `while read linha` | Lê cada linha e armazena na variável `linha` |
| `done < arquivo.txt` | Indica qual arquivo será lido |

---

## 🛠️ 3. Exemplo básico

Suponha que o arquivo `nomes.txt` contenha:

```
Ana
Bruno
Carlos
```

### Script:

```bash
#!/bin/bash

while read nome
do
    echo "Olá, $nome!"
done < nomes.txt
```

> Saída:
```
Olá, Ana!
Olá, Bruno!
Olá, Carlos!
```

---

## 🔄 4. Lendo arquivos com espaços

Por padrão, o `read` **divide a linha em palavras**.

Para preservar a linha inteira, use:

```bash
while IFS= read -r linha
do
    echo "Linha completa: $linha"
done < arquivo.txt
```

| Elemento | Função |
|:---|:---|
| `IFS=` | Evita remover espaços em branco |
| `-r` | Impede que barras invertidas sejam interpretadas |

---

## 🧠 5. Exemplo avançado: Numerar linhas

```bash
#!/bin/bash

contador=1

while IFS= read -r linha
do
    echo "$contador: $linha"
    contador=$((contador + 1))
done < arquivo.txt
```

> Saída:
```
1: Ana
2: Bruno
3: Carlos
```

---

## ⚡ 6. Lendo diretamente de comandos

Você pode usar `while read` com a saída de outros comandos:

```bash
ls | while read arquivo
do
    echo "Arquivo encontrado: $arquivo"
done
```

> Lê cada linha da saída do `ls` como uma entrada.

---

## 🎯 Boas práticas

- Sempre usar `IFS= read -r` para evitar problemas com espaços e caracteres especiais.
- Verificar se o arquivo existe antes de ler.
- Usar nomes claros para as variáveis (`linha`, `entrada`, etc).

---
