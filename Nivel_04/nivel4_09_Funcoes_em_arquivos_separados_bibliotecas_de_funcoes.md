
# 🔵 Nível 4 — Tópico 9: Funções em Arquivos Separados (Bibliotecas de Funções)

---

## 📖 1. O que são bibliotecas de funções no Bash?

Bibliotecas de funções são **arquivos que contêm apenas funções** que podem ser reutilizadas em vários scripts.

✅ Evitam repetição de código  
✅ Organizam o projeto  
✅ Facilitam manutenção e expansão

> Exatamente como em outras linguagens de programação.

---

## 📦 2. Estrutura sugerida de projeto com bibliotecas

```
meu_projeto/
├── principal.sh
└── libs/
    ├── funcoes_arquivo.sh
    └── funcoes_validacao.sh
```

**libs/** → Guardam os módulos (bibliotecas de funções)  
**principal.sh** → Script principal que importa e usa as funções

---

## 📚 3. Exemplo de biblioteca simples

### 📄 libs/funcoes_arquivo.sh

```bash
exibir_arquivo() {
    if [ -f "$1" ]; then
        cat "$1"
    else
        echo "Arquivo não encontrado: $1"
    fi
}
```

### 📄 libs/funcoes_validacao.sh

```bash
validar_numero() {
    if [[ "$1" =~ ^[0-9]+$ ]]; then
        echo "Número válido."
    else
        echo "Não é um número."
    fi
}
```

---

## 🚦 4. Como carregar bibliotecas no script principal

```bash
#!/bin/bash

# Carregar bibliotecas
source libs/funcoes_arquivo.sh
source libs/funcoes_validacao.sh

# Usar funções
exibir_arquivo "meuarquivo.txt"
validar_numero "1234"
```

> Com `source`, as funções ficam disponíveis como se estivessem no mesmo arquivo.

---

## 🚨 5. Boas práticas para bibliotecas

- ❗ NÃO inclua comandos fora das funções (evitar execuções inesperadas)
- ✅ Dê nomes claros e prefixados para evitar conflitos (ex: `valida_*`, `arquivo_*`)
- ✅ Documente cada função com comentários
- ✅ Separe bibliotecas por tema (validações, arquivos, usuários...)

---

## 📌 6. Exemplo completo e organizado

```
meu_projeto/
├── principal.sh
├── libs/
│   ├── arquivos.sh
│   └── validacoes.sh
└── data/
    └── arquivo_teste.txt
```

```bash
# libs/arquivos.sh

exibir_conteudo() {
    cat "$1"
}
```

```bash
# libs/validacoes.sh

checar_vazio() {
    if [ -z "$1" ]; then
        echo "Está vazio"
    else
        echo "Conteúdo OK"
    fi
}
```

```bash
# principal.sh

source libs/arquivos.sh
source libs/validacoes.sh

exibir_conteudo "data/arquivo_teste.txt"
checar_vazio ""
```

> Organização clara e código fácil de reutilizar e manter.

---

## 🎯 Conclusão

- Bibliotecas são arquivos que contêm funções reutilizáveis.
- `source` integra bibliotecas ao script principal.
- Boas práticas tornam bibliotecas seguras e fáceis de manter.

---
