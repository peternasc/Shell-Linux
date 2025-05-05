
# 🔵 Nível 4 – Tópico 2: Escopo — Variáveis Locais e Globais

---

## 📖 1. O que é escopo de variáveis?

**Escopo** é o que define **onde uma variável pode ser acessada** dentro do script.

Existem dois tipos principais:

| Tipo | Onde é acessível |
| ---- | ---------------- |
| Global | Em qualquer lugar do script |
| Local | Somente dentro da função onde foi declarada |

---

## 📚 2. Variáveis globais

### 📌 Exemplo básico

```bash
#!/bin/bash

mensagem="Olá, mundo!"

exibir_mensagem() {
    echo "$mensagem"
}

exibir_mensagem
```

> A função acessa normalmente a variável global `mensagem`.

---

## 🚨 3. Problema com variáveis globais

**Variáveis globais podem ser sobrescritas sem querer!**

```bash
#!/bin/bash

contador=0

incrementar() {
    contador=$((contador + 1))
}

incrementar
incrementar

echo "Contador: $contador"
```

> A função modificou a variável global `contador` sem que fosse a intenção.

---

## 🔐 4. Variáveis locais com `local`

Para **proteger variáveis dentro da função**, usamos `local`:

```bash
#!/bin/bash

minha_funcao() {
    local contador=0
    contador=$((contador + 1))
    echo "Dentro da função: $contador"
}

minha_funcao
minha_funcao

echo "Fora da função: $contador"
```

> `contador` não existe fora da função. Está seguro dentro dela.

---

## ✅ 5. Boas práticas

- Prefira **variáveis locais** em funções para evitar problemas.
- Use **globais apenas quando necessário** (como em configurações).
- Sempre inicialize variáveis locais.

---

## 📚 6. Exemplo completo (global e local juntos)

```bash
#!/bin/bash

mensagem_global="Script iniciado."

mostrar_mensagem() {
    local mensagem_local="Executando função..."
    echo "$mensagem_local"
    echo "$mensagem_global"
}

mostrar_mensagem

echo "Finalizando script."
```

> A função acessa a global, mas mantém a local isolada.

---

## 🎯 Conclusão

- **`local` protege variáveis dentro das funções**
- **Globais estão acessíveis em qualquer lugar, mas são arriscadas**
- **Boas práticas pedem o uso de `local` sempre que possível**

---
