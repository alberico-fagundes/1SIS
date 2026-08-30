# 🐍 MT-02 (Pre-Sequel) - O HACK DO MINICONDA
## Engenharia de Software ULTRA DIDÁTICA | SaaS Smart Academy Reborn

> **🎯 OBJETIVO EXTRAORDINÁRIO:** Você está num computador bloqueado e não tem a senha de Administrador (sudo) para instalar o Git? Vamos usar um "Cavalo de Troia" do bem chamado **Miniconda**. Ele é um instalador furtivo que coloca programas gigantescos na sua máquina escondidos dentro da sua pasta de usuário, onde o administrador não manda nada!

---

## 🪄 O FEITIÇO PASSO A PASSO (INSTALAÇÃO)

Abra o seu terminal (no Linux ou WSL) e copie/cole um comando por vez. Espere cada comando terminar antes de colar o próximo:

**1. O Download Furtivo:**
Baixa o instalador do Miniconda sem abrir o navegador.
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
```

**2. A Instalação Silenciosa:**
Instala o Miniconda na sua pasta pessoal de forma invisível (sem te fazer perguntas chatas).
```bash
bash ~/miniconda.sh -b -p $HOME/miniconda3
```

**3. Ligando o Motor:**
Injeta o poder do Conda no terminal que você está usando agora.
```bash
source ~/miniconda3/bin/activate
```

**4. A Configuração Eterna:**
Ensina o computador a ligar o Conda automaticamente sempre que você abrir um terminal novo.
```bash
conda init
```

**O TESTE FINAL:**
Feche o VSCode (ou o terminal) e abra de novo.
Se apareceu a palavra `(base)` no início da linha do seu terminal, **o hack funcionou!** Você enganou o sistema operacional.

---

## 🧰 INSTALANDO O GIT SEM SENHA

Agora que o Miniconda está rodando, nós ganhamos acesso ao "Mercado Negro" de aplicativos. O Conda pode baixar ferramentas poderosas diretamente para a sua pasta de usuário.

No terminal (que agora tem o `(base)` escrito), digite:

```bash
conda install git -y
```
*(O `-y` no final significa "Sim para tudo", para você não precisar nem apertar Enter de novo).*

Pronto! Digite `git --version` para ver a mágica. O Git está instalado e funcionando perfeitamente, e o computador nem pediu a senha de Administrador.

---

## 🔮 O FUTURO (Por que o Conda é incrível?)

Nós usamos o Miniconda hoje só para instalar o Git e fugir do bloqueio.
Mas no **Módulo MT04 (Inteligência Artificial)**, nós precisaremos instalar ferramentas pesadas de dados como `Pandas` e `Scikit-Learn`. O Conda será o nosso melhor amigo lá também, pois ele cria "Bolhas" isoladas para que um projeto nunca quebre o outro. 

Mas, por hoje, a sua missão está cumprida. Volte para o Desafio do Faunadex e faça os seus commits!
