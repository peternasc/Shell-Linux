
# 🔵 Nível 4 — Tópico 5: Estrutura Modular de Scripts Grandes

---

## 📖 1. Por que modularizar scripts grandes?

À medida que scripts crescem, eles podem:

❗ Ficar difíceis de ler  
❗ Ser difíceis de manter  
❗ Ter funções e lógicas repetidas

**Modularizar** resolve esses problemas:

✅ Torna o código organizado e fácil de navegar  
✅ Permite reutilização de funções e trechos  
✅ Facilita manutenção e atualizações

---

## 📚 2. Como dividir scripts em arquivos menores

### Estratégia

- **Scripts principais**: Contêm o fluxo principal do programa.
- **Módulos/funções**: Contêm funções e rotinas específicas.
- **Configurações**: Variáveis e parâmetros globais.

### Exemplo de organização

```
meu_projeto/
├── principal.sh
├── libs/
│   ├── funcoes.sh
│   └── validacoes.sh
└── config/
    └── variaveis.sh
```

---

## 📦 3. Usando `source` para integrar módulos

No `principal.sh`:

```bash
#!/bin/bash

# Importar configurações e funções
source config/variaveis.sh
source libs/funcoes.sh
source libs/validacoes.sh

# Exemplo de uso
mostrar_boas_vindas
validar_usuario "Peterson"
```

Nos arquivos de funções:

```bash
# funcoes.sh

mostrar_boas_vindas() {
    echo "Bem-vindo ao sistema, $USUARIO!"
}
```

```bash
# validacoes.sh

validar_usuario() {
    if [ "$1" == "$USUARIO" ]; then
        echo "Usuário válido."
    else
        echo "Usuário inválido."
    fi
}
```

```bash
# variaveis.sh

USUARIO="Peterson"
```

> Modularidade em ação: cada parte do sistema é isolada, clara e reutilizável.

---

## 🚦 4. Boas práticas para modularização

- **Organize pastas** — Use `libs`, `config`, `scripts` para separar arquivos.  
- **Nomeie arquivos e funções claramente** — Exemplo: `validacoes.sh`, `log_util.sh`.  
- **Carregue módulos no início do script principal** — Use `source` para importar.  
- **Mantenha funções pequenas e específicas** — Uma função → Uma responsabilidade.  
- **Documente funções nos arquivos de módulo** — Ajuda a entender o propósito.

---

## 🎯 5. Exemplo de execução (fluxo completo)

```bash
./principal.sh
```

Saída:

```
Bem-vindo ao sistema, Peterson!
Usuário válido.
```

> Fluxo claro e fácil de manter!

---

## ✅ Conclusão

- Modularizar melhora a organização e a manutenção de scripts.
- `source` é o elo que conecta módulos ao script principal.
- Organize suas pastas e arquivos para projetos profissionais.

---
