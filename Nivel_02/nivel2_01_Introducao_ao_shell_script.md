
# 🟣 Nível 2 – Tópico 1: Introdução ao Shell Script

---

## 📖 1. O que é um Shell Script?

Um **Shell Script** é simplesmente **um conjunto de comandos escritos em um arquivo de texto**, que o terminal (o Shell) pode interpretar e executar **linha por linha**.

- **Shell** → é o programa que interpreta comandos (como o Bash).
- **Script** → é uma sequência de instruções gravadas em um arquivo.

Portanto, **Shell Script** = um arquivo contendo **comandos de terminal organizados** para serem executados automaticamente.

---

## 🧠 2. Para que serve um Shell Script?

- Automatizar tarefas repetitivas (backups, atualizações, instalação de programas)
- Criar **instaladores** e **ferramentas internas**
- Realizar **verificações automáticas** (como checar espaço em disco)
- Automatizar **gerenciamento de usuários, permissões** e muito mais
- Integrar **processos do sistema** de maneira segura e padronizada

---

## ⚙️ 3. Como é um Shell Script básico?

Todo Shell Script precisa:

- Um **arquivo de texto simples** (sem formatação, tipo `.sh`)
- Uma **linha especial no começo** chamada **shebang**:
  ```bash
  #!/bin/bash
  ```

Essa linha diz ao sistema que o script deve ser interpretado pelo **Bash**.

### Exemplo mínimo:

```bash
#!/bin/bash
echo "Olá, mundo!"
```

---

## 📂 4. Diferença entre digitar no terminal e criar um script

| Terminal direto | Shell Script (.sh) |
|:---|:---|
| Você digita manualmente os comandos | Você grava os comandos em um arquivo |
| Depois que executa, eles desaparecem | Você pode reusar e modificar sempre que quiser |
| Ideal para tarefas pontuais | Ideal para tarefas repetitivas ou complexas |

---

## 🔥 5. Fluxo básico de criação de um script

### 1. Criar um arquivo `.sh`
```bash
nano meu_script.sh
```

### 2. Escrever o conteúdo (incluindo o `#!/bin/bash` no topo)
```bash
#!/bin/bash
echo "Executando meu primeiro script!"
```

### 3. Dar permissão de execução
```bash
chmod +x meu_script.sh
```

### 4. Executar o script
```bash
./meu_script.sh
```

---

## 🛠️ 6. Boas práticas iniciais

- Sempre comece o script com `#!/bin/bash`
- Use nomes de arquivos **sem espaços** e de preferência **minúsculos**
- Comente seu código usando `#` para explicar partes importantes
- Torne seu script executável com `chmod +x`
- Teste seu script **em partes pequenas** antes de rodar tudo

---

## 🧠 7. Curiosidade

O Shell Script é uma **linguagem interpretada**:  
Isso significa que **não precisa compilar** — o Bash interpreta linha por linha na hora de executar.
