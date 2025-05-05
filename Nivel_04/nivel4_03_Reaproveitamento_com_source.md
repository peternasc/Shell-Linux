
# 🔵 Nível 4 – Tópico 3: Reaproveitamento com `source`

---

## 📖 1. O que é o comando `source`

O comando `source` (ou o símbolo `.` que faz o mesmo) permite **executar um arquivo no contexto atual do shell**.

Isso é útil porque:

✅ Permite carregar funções de outro arquivo  
✅ Permite carregar variáveis de configuração  
✅ NÃO inicia um novo processo — tudo acontece no mesmo ambiente

---

## 📚 2. Como usar o `source`

### 📌 Exemplo básico

```bash
source meu_script.sh
# ou
. meu_script.sh
```

Isso executará o script **no contexto atual**, ou seja:

- Variáveis definidas no script ficarão disponíveis
- Funções definidas no script poderão ser chamadas

---

## 📦 3. Exemplo prático com funções

### 📄 Arquivo: `funcoes.sh`

```bash
dizer_ola() {
    echo "Olá, $1!"
}
```

### 📄 Arquivo: `principal.sh`

```bash
#!/bin/bash

# Carregar funções
source funcoes.sh

# Usar função importada
dizer_ola "Peterson"
```

> Saída:

```
Olá, Peterson!
```

---

## 🚨 4. Diferença entre source e executar diretamente

| Ação | O que acontece |
| ---- | --------------- |
| `bash script.sh` | Executa em um NOVO processo, variáveis e funções morrem no final |
| `source script.sh` | Executa no MESMO processo, mantendo variáveis e funções ativas |

---

## 📚 5. Organizando seus scripts com source

### Organização sugerida:

```
meu_projeto/
├── libs/
│   ├── funcoes.sh
│   └── utilidades.sh
├── principal.sh
```

Em `principal.sh`, você pode carregar todos:

```bash
source libs/funcoes.sh
source libs/utilidades.sh
```

Isso deixa o script **modular e organizado**.

---

## 🎯 6. Boas práticas

- Use `source` para importar **funções comuns e configurações**
- Não use para rodar scripts que devem ser independentes
- Use nomes claros nos arquivos que serão importados (ex: `funcoes.sh`, `config.sh`)

---

## 📌 7. Exemplo avançado (Parâmetros e funções compartilhadas)

### 📄 Arquivo: `config.sh`

```bash
USUARIO="Peterson"
```

### 📄 Arquivo: `funcoes.sh`

```bash
dizer_ola() {
    echo "Olá, $USUARIO!"
}
```

### 📄 Arquivo: `principal.sh`

```bash
#!/bin/bash

source config.sh
source funcoes.sh

dizer_ola
```

> Saída:

```
Olá, Peterson!
```

---

## ✅ Conclusão

- `source` é ideal para **reutilização de código e configuração**.  
- Evite rodar scripts independentes com `source`.  
- Organize seus scripts em pastas e carregue funções e variáveis com clareza.

---
