
# Apêndice – Comando `whoami`

---

## 📖 1. O que é o comando `whoami`?

O `whoami` é um comando Unix/Linux que responde à pergunta:  
**“Quem sou eu neste sistema agora?”**

Ou seja, ele retorna o **nome do usuário efetivo atual (EUID)** da sessão onde o comando é executado.

---

## ⚙️ 2. Como funciona?

Internamente, `whoami` consulta o **EUID** (Effective User ID) da sessão e **resolve o nome associado** a ele.

### Exemplo:
```bash
whoami
```

> Saída típica:
```
peterson
```

Se você rodar com `sudo`:
```bash
sudo whoami
```
> Saída:
```
root
```

---

## 🧠 3. Quando e por que usar `whoami`?

- Verificar **qual usuário está ativo**
- Garantir que está como **root** antes de instalar algo ou rodar scripts
- Em **scripts automatizados**, limitar ações por usuário
- Ambientes com **vários usuários ou conexões SSH**

---

## 🛠️ 4. Exemplos práticos

### Ver usuário atual:
```bash
whoami
```

### Ver se você tem poderes administrativos:
```bash
sudo whoami
```

### Validar usuário antes de executar algo:
```bash
if [ "$(whoami)" != "root" ]; then
  echo "Execute como root!"
  exit 1
fi
```

---

## 📂 5. Comandos relacionados

| Comando     | O que faz |
|-------------|-----------|
| `id`        | Mostra UID, GID e grupos do usuário atual |
| `logname`   | Mostra o usuário que **fez login** na sessão |
| `who`       | Lista todos os usuários conectados no momento |
| `users`     | Lista os nomes de todos os usuários conectados |
| `id -un`    | Exibe o mesmo que `whoami` |

---

## 📋 6. Opções e flags do `whoami`

| Flag          | Significado                        |
|---------------|-------------------------------------|
| `--help`      | Exibe ajuda e uso do comando        |
| `--version`   | Mostra a versão do utilitário       |

### Exemplos:
```bash
whoami --help
whoami --version
```

> Essas flags funcionam apenas em sistemas com GNU/Linux.  
> Em algumas distros minimalistas ou BSDs, `whoami` pode não aceitar nenhuma opção.

---

## 🧠 Dica bônus

Você pode usar `whoami` junto com outras funções em scripts ou status do sistema:

```bash
echo "Olá, $(whoami)! Seja bem-vindo ao seu terminal."
```
