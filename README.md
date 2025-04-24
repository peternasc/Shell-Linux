
# 🐧 Bash para Gerenciamento de Sistemas e Aplicações (Modo Terminal Puro)

Este repositório é meu guia definitivo de estudos em Bash, com foco total em **administração de sistemas**, **automação de tarefas**, **monitoramento**, **segurança**, e **integração com aplicações e serviços** — **tudo isso 100% em terminal, sem interface gráfica**.  
O plano vai do nível **mais básico possível** até o **super hiper mega avançado**. 🚀

---

## 📘 Estrutura dos Estudos

- ✅ Estilo checklist: cada item pode ser marcado conforme for estudado
- 🔁 Dividido por níveis: do zero ao lendário
- 💻 Foco total em administração de sistemas com Bash
- 🧱 Compatível com servidores, máquinas virtuais, Raspberry Pi headless e sistemas Linux sem GUI

---

## 🟤 Nível 0 – Pré-Básico: Primeiros Passos no Terminal

- [x] [O que é terminal? O que é Bash?](Nivel_00/nivel0_01_O_que_e_terminal_O_que_e_Bash.md)
- [x] [Entendendo o shell e seu papel no sistema](Nivel_00/nivel0_02_Entendendo_o_shell_e_seu_papel_no_sistema.md)
- [x] [Como usar o terminal puro (sem interface gráfica)](Nivel_00/nivel0_03_Como_usar_o_terminal_puro.md)
- [x] [Como digitar comandos corretamente](Nivel_00/nivel0_04_Como_digitar_comandos_corretamente.md)
- [x] [Navegação básica: `pwd`, `cd`, `ls`](Nivel_00/nivel0_05_Navegacao_basica_pwd_cd_ls.md)
- [x] [Como sair de comandos travados (`Ctrl + C`)](Nivel_00/nivel0_06_Como_sair_de_comandos_travados.md)
- [x] [Usar seta ↑ para comandos anteriores](Nivel_00/nivel0_07_Usar_seta_para_comandos_anteriores.md)
- [x] [Autocompletar com `Tab`](Nivel_00/nivel0_08_Autocompletar_com_Tab.md)

---

## 🟢 Nível 1 – Básico: Comandos Essenciais e Estrutura de Arquivos

- [ ] Estrutura de diretórios do Linux (`/home`, `/etc`, `/var`, etc.)
- [ ] Criação e manipulação de arquivos e pastas: `touch`, `mkdir`, `cp`, `mv`, `rm`
- [ ] Permissões e propriedade de arquivos: `chmod`, `chown`, `ls -l`
- [ ] Leitura de arquivos com `cat`, `less`, `head`, `tail`
- [ ] Redirecionamento de entrada e saída: `>`, `>>`, `<`
- [ ] Encadeamento com pipes: `|`
- [ ] Comandos úteis do sistema: `whoami`, `clear`, `history`, `file`

---

## 🟡 Nível 2 – Bash Script Iniciante

- [ ] Criar e executar scripts (`.sh`, `chmod +x`)
- [ ] Variáveis simples (`nome="Peterson"`)
- [ ] Exibir informações com `echo`
- [ ] Leitura de entrada com `read`
- [ ] Uso de parâmetros (`$1`, `$@`, `$#`)
- [ ] Condições simples com `if`, `then`, `fi`
- [ ] Comentários com `#`

---

## 🟠 Nível 3 – Bash Script Estruturado

- [ ] Condicionais completas: `if/elif/else`
- [ ] `case` para múltiplas opções
- [ ] Laços: `for`, `while`, `until`
- [ ] Controle de fluxo: `break`, `continue`
- [ ] Menus com `select`
- [ ] Códigos de retorno e uso de `$?`

---

## 🔵 Nível 4 – Organização e Modularização de Scripts

- [ ] Criação e uso de funções
- [ ] Escopo: variáveis locais e globais
- [ ] Reaproveitamento com `source`
- [ ] Boas práticas e cabeçalhos de script
- [ ] Estrutura modular de scripts grandes
- [ ] Registro e logs simples em arquivos `.log`

---

## 🟣 Nível 5 – Administração de Sistemas Automatizada

- [ ] Verificar espaço em disco: `df`, `du`, `ncdu`
- [ ] Monitoramento de RAM e CPU: `free`, `top`, `htop`, `uptime`
- [ ] Gerenciar processos: `ps`, `kill`, `nice`, `renice`
- [ ] Agendando tarefas: `cron`, `at`, `anacron`
- [ ] Automatizar atualizações com `apt`, `yum`, `dnf`
- [ ] Backups com `tar`, `gzip`, `rsync`
- [ ] Menus interativos em terminal com `dialog` e `whiptail` (modo texto)

---

## 🟥 Nível 6 – Manipulação de Dados e Logs com Bash

- [ ] `grep`, `cut`, `sort`, `uniq`, `xargs`
- [ ] `awk` básico e intermediário
- [ ] `sed` para substituições e transformações
- [ ] Utilitários: `tr`, `paste`, `join`, `split`
- [ ] Manipular `.csv` e `.json` com `jq`
- [ ] Gerar relatórios em terminal (com alinhamento e contagem)

---

## 🔶 Nível 7 – Segurança e Diagnóstico

- [ ] Ver logs do sistema: `journalctl`, `tail -f /var/log/*`
- [ ] Detectar falhas automaticamente (criar analisadores simples)
- [ ] Analisar conexões de rede: `netstat`, `ss`, `lsof`, `nmap`
- [ ] Bloquear IPs com `iptables`, `ufw`, `fail2ban`
- [ ] Verificar permissões de diretórios sensíveis
- [ ] Criptografar e descriptografar arquivos com `gpg`, `openssl`
- [ ] Detectar e registrar logins suspeitos

---

## ⚫ Nível 8 – Integrações e APIs com Bash

- [ ] Enviar mensagens para Telegram, Slack ou Discord via Bash
- [ ] Fazer requisições HTTP com `curl`
- [ ] Interpretar e processar JSON com `jq`
- [ ] Autenticação com token em APIs REST
- [ ] Usar APIs públicas e privadas (clima, moedas, GitHub etc.)
- [ ] Integrações com repositórios, serviços e bancos de dados

---

## 👑 Nível 9 – Terminal Supremo: Autonomia Total

- [ ] Segurança com `set -e`, `set -u`, `trap`, `pipefail`
- [ ] Scripts autorreparáveis (auto-healing)
- [ ] Debug profissional com `bash -x`, `strace`, `lsof`, `dmesg`
- [ ] Automatização de containers: `docker`, `podman`, `lxc`
- [ ] Scripts que geram outros scripts automaticamente
- [ ] Interfaces ricas em terminal com `dialog`, `whiptail`, `fzf`
- [ ] Automação de infraestrutura via Bash: AWS CLI, GCP, Terraform

---

## 📌 Como usar

Clone este repositório, estude com calma e marque `[x]` cada item conforme for concluindo.  
O plano é longo, mas te leva do zero ao topo do Bash como ferramenta de automação e gerenciamento de sistemas Linux! 💪🐧
