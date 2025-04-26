
# 🟣 Nível 2 – Tópico 6: Uso de Parâmetros (`$1`, `$@`, `$#`)

---

## 📖 1. O que são parâmetros em Shell Script?

Parâmetros são **valores enviados ao script** **na hora da execução**, diretamente pela linha de comando.

- Você passa informações externas sem precisar alterá-las dentro do script.
- Torna o script **mais flexível e reutilizável**.

---

## 📋 2. Como acessar os parâmetros?

| Símbolo | O que faz |
|:---|:---|
| `$1`, `$2`, `$3`, etc. | Acessa o 1º, 2º, 3º parâmetro individualmente |
| `$@` | Acessa **todos** os parâmetros como uma lista |
| `$#` | Informa o **número total** de parâmetros recebidos |

---

## 🛠️ 3. Exemplo básico usando `$1`

### Script `meu_script.sh`:

```bash
#!/bin/bash

echo "Olá, $1!"
```

### Executando:

```bash
./meu_script.sh Peterson
```

> Saída:
```
Olá, Peterson!
```

---

## 🧩 4. Exemplo com múltiplos parâmetros

### Script `dados.sh`:

```bash
#!/bin/bash

echo "Nome: $1"
echo "Idade: $2"
echo "Cidade: $3"
```

### Executando:

```bash
./dados.sh Peterson 35 "São Paulo"
```

> Saída:
```
Nome: Peterson
Idade: 35
Cidade: São Paulo
```

---

## 📚 5. Usando `$@` para pegar todos os parâmetros

`$@` permite percorrer todos os parâmetros enviados.

### Exemplo:

```bash
#!/bin/bash

for parametro in "$@"
do
  echo "Recebido: $parametro"
done
```

### Executando:

```bash
./meusdados.sh Um Dois Tres
```

> Saída:
```
Recebido: Um
Recebido: Dois
Recebido: Tres
```

---

## 📈 6. Usando `$#` para contar parâmetros

`$#` mostra **quantos argumentos** foram passados ao script.

### Exemplo:

```bash
#!/bin/bash

echo "Você forneceu $# argumentos."
```

### Executando:

```bash
./conta.sh um dois tres
```

> Saída:
```
Você forneceu 3 argumentos.
```

---

## 🎯 Boas práticas

- Sempre **validar** se o número esperado de argumentos foi passado.
- Usar `"$@"` sempre com aspas para preservar espaços em argumentos compostos (como "São Paulo").

---

### Exemplo de validação:

```bash
#!/bin/bash

if [ "$#" -ne 2 ]; then
  echo "Uso correto: $0 nome idade"
  exit 1
fi

echo "Olá, $1! Você tem $2 anos."
```
