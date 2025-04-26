
# 🟣 Nível 2 – Tópico 2: Criar e Executar Scripts (.sh, `chmod +x`)

---

## 📖 1. O que é um script `.sh`?

No Linux, **scripts de shell** geralmente têm a extensão `.sh`, que indica que são arquivos de **Shell Script**.

Essa extensão é **opcional**, mas é uma prática recomendada para deixar claro que o arquivo contém comandos para serem interpretados pelo Shell (como o Bash).

---

## ⚙️ 2. Como criar um script `.sh`?

### 1. Criar o arquivo

Use qualquer editor de texto simples:

```bash
nano meu_script.sh
```
ou
```bash
vim meu_script.sh
```
ou
```bash
touch meu_script.sh
```

---

### 2. Adicionar conteúdo básico ao arquivo

Comece sempre com a linha chamada **shebang**:

```bash
#!/bin/bash
```

Depois, escreva os comandos que deseja executar.

### Exemplo:
```bash
#!/bin/bash
echo "Esse é meu primeiro script executável!"
```

Salve e feche o arquivo (`Ctrl + O`, `Enter`, `Ctrl + X` no `nano`).

---

## 🔒 3. Permitir a execução do script (`chmod +x`)

Por padrão, arquivos recém-criados **não são executáveis** no Linux.  
Você precisa dar a **permissão de execução** com o comando `chmod`.

### Comando:
```bash
chmod +x meu_script.sh
```

- `chmod` = change mode (alterar permissões)
- `+x` = adicionar permissão de execução (execute)
- `meu_script.sh` = o arquivo que você quer tornar executável

---

## 🏃 4. Como executar o script?

Existem duas formas principais:

### 1. Executar diretamente com `./`:

```bash
./meu_script.sh
```

Aqui `./` significa "execute o arquivo que está no diretório atual".

---

### 2. Executar com o interpretador explícito:

```bash
bash meu_script.sh
```

Essa forma **não exige** permissão de execução (`chmod +x`), pois você está chamando diretamente o interpretador.

---

## 🧠 5. Dicas importantes

- Sempre adicione `#!/bin/bash` no topo para garantir que o Bash será usado, mesmo que seu sistema tenha outro shell padrão.
- Mantenha seus scripts em pastas específicas, como `~/scripts` para organizar melhor.
- Scripts **não precisam obrigatoriamente** ter extensão `.sh`, mas usar `.sh` ajuda a identificar rapidamente seu propósito.
- Use `chmod -x` se quiser **remover** a permissão de execução de um script.
- Para rodar um script de **qualquer lugar**, você pode mover o script para uma pasta que esteja no seu **PATH**, como `/usr/local/bin`.

---

## 📂 Exemplo completo passo a passo

### Criar um script
```bash
nano ola.sh
```

### Conteúdo:
```bash
#!/bin/bash
echo "Olá, Peterson! Este é seu script!"
```

### Dar permissão:
```bash
chmod +x ola.sh
```

### Executar:
```bash
./ola.sh
```

> Saída:
```
Olá, Peterson! Este é seu script!
```
