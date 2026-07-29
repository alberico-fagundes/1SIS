# 🚀 DESAFIO 01 - A ARENA FAUNADEX (A CONSTRUÇÃO PASSO A PASSO)
## Engenharia de Software ULTRA DIDÁTICA | SaaS Smart Academy Reborn

> **🎯 OBJETIVO EXTRAORDINÁRIO:** Seu cérebro não aprende copiando um código gigante de uma vez. Ele aprende quebrando problemas grandes em pedacinhos minúsculos (Baby Steps). Vamos construir a Arena de Duelo do **Faunadex** (estilo Triple Triad do Final Fantasy 8) tijolo por tijolo. E a regra de ouro: A cada tijolo assentado, nós salvamos o jogo (Git Commit).

---

## 🃏 O CONCEITO DO TABULEIRO
O nosso jogo terá:
- **Coluna Esquerda:** Sua Mão (5 cartas).
- **Coluna Central:** A Mesa de Batalha (Grid de 3x3 = 9 espaços).
- **Coluna Direita:** Mão do Inimigo (5 cartas).

Parece difícil? Vamos dominar o **CSS Grid** e resolver isso em 4 passos. Crie um arquivo `index.html` e vamos começar.

---

## 🏗️ PASSO 1: O ESQUELETO VAZIO E A PINTURA BASE

A primeira coisa é montar a estrutura HTML sem beleza nenhuma, apenas caixas vazias.

**1.** Copie o código abaixo no seu `index.html`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Faunadex Arena</title>
    <style>
        body {
            background-color: #1a1a2e; /* Fundo noturno */
            color: white;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh; /* Tela inteira */
        }
        
        /* Apenas cores temporárias para enxergarmos as caixas */
        .arena { background-color: #16213e; padding: 20px; }
        .mao-aliado { border: 2px solid green; }
        .tabuleiro { border: 2px solid blue; }
        .mao-inimigo { border: 2px solid red; }
    </style>
</head>
<body>
    <!-- A CAIXA PAI (Onde tudo acontece) -->
    <div class="arena">
        
        <div class="mao-aliado">
            Mão Esquerda (Em breve 5 cartas)
        </div>

        <div class="tabuleiro">
            Mesa Central (Em breve 9 espaços)
        </div>

        <div class="mao-inimigo">
            Mão Direita (Em breve 5 cartas)
        </div>

    </div>
</body>
</html>
```
Abra no navegador. Você verá as três divs empilhadas uma em cima da outra. Feio, não é? Vamos salvar e consertar isso.

💾 **O SAVE GAME OBRIGATÓRIO (No Terminal):**
```bash
git add .
git commit -m "Passo 1: Esqueleto HTML e fundo escuro criados"
```

---

## 📐 PASSO 2: O MILAGRE DO CSS GRID (AS 3 COLUNAS)

No comportamento padrão da Web, as "caixas" caem de cima para baixo. Nós queremos colocar a Mão, a Mesa e o Inimigo **lado a lado**.

Vá na tag `<style>` do seu arquivo e **adicione/modifique** o CSS da classe `.arena` para isso:

```css
        .arena { 
            background-color: #16213e; 
            padding: 30px; 
            border-radius: 15px;
            
            /* O SEGREDO DO ARQUITETO */
            display: grid;
            /* Eu quero 3 colunas: A primeira com 150px, a do meio com 450px e a última com 150px */
            grid-template-columns: 150px 450px 150px;
            gap: 40px; /* Um corredor de 40px separando as colunas */
        }
```

Atualize o navegador (`F5`). **BUM!** Magicamente as três áreas estão uma do lado da outra perfeitamente alinhadas.

💾 **O SAVE GAME OBRIGATÓRIO (No Terminal):**
```bash
git add .
git commit -m "Passo 2: Implementado CSS Grid com 3 colunas principais"
```

---

## 🖐️ PASSO 3: CRIANDO AS 5 CARTAS NA MÃO

Agora vamos focar nas pontas. O jogador precisa segurar 5 cartas uma embaixo da outra (um grid de 5 Linhas por 1 Coluna).

**1.** Vá no HTML (lá embaixo) e substitua os textos da `mao-aliado` e `mao-inimigo` por 5 caixas menores:

```html
        <div class="mao-aliado">
            <div class="carta">Carta 1</div>
            <div class="carta">Carta 2</div>
            <div class="carta">Carta 3</div>
            <div class="carta">Carta 4</div>
            <div class="carta">Carta 5</div>
        </div>

        <!-- Pule o tabuleiro por enquanto... e faça o mesmo no inimigo -->

        <div class="mao-inimigo">
            <div class="carta inimigo">Inimigo 1</div>
            <div class="carta inimigo">Inimigo 2</div>
            <div class="carta inimigo">Inimigo 3</div>
            <div class="carta inimigo">Inimigo 4</div>
            <div class="carta inimigo">Inimigo 5</div>
        </div>
```

**2.** Volte lá em cima no `<style>` e adicione a regra das Mãos:
```css
        /* Transformando a Mão em um Grid de 5 linhas */
        .mao-aliado, .mao-inimigo {
            display: grid;
            grid-template-rows: repeat(5, 120px); /* 5 linhas de 120px de altura */
            gap: 15px;
            border: none; /* Tirando a borda feia do Passo 1 */
        }

        /* Desenhando a Carta */
        .carta {
            background-color: #0f3460;
            border: 2px dashed #4CAF50; /* Borda Verde Tracejada */
            border-radius: 8px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Cartas do Inimigo ficam vermelhas */
        .inimigo {
            border-color: #e94560;
            color: #e94560;
        }
```
Atualize o navegador. Suas 5 cartas verdes na esquerda e 5 vermelhas na direita nasceram!

💾 **O SAVE GAME OBRIGATÓRIO:**
```bash
git add .
git commit -m "Passo 3: Layout de 5 cartas criado para aliado e inimigo"
```

---

## 🎲 PASSO 4: O CAMPO DE BATALHA (A MESA 3x3)

O último desafio é o mais importante. O meio da mesa precisa ser uma matriz perfeita de 3x3. Como o `CSS Grid` faz isso de olhos fechados? Nós pedimos `repeat(3)`.

**1.** No HTML, substitua o texto dentro da `<div class="tabuleiro">` por 9 caixinhas:
```html
        <div class="tabuleiro">
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
            <div class="slot">Mesa</div>
        </div>
```

**2.** Suba no `<style>` e adicione o Feitiço do Tabuleiro:
```css
        .tabuleiro {
            display: grid;
            /* Magia Pura: 3 colunas iguais, 3 linhas iguais */
            grid-template-columns: repeat(3, 1fr); 
            grid-template-rows: repeat(3, 140px);
            gap: 10px;
            
            background-color: #0d1b2a;
            border: 3px solid #e94560;
            border-radius: 10px;
            padding: 15px;
        }

        .slot {
            background-color: #1b263b;
            border: 1px solid #415a77;
            border-radius: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: 0.3s;
        }

        /* Efeito ao passar o mouse */
        .slot:hover {
            background-color: #4CAF50;
            cursor: pointer;
        }
```

Atualize o navegador. **A TRÍADE ESTÁ COMPLETA!** Você criou um tabuleiro complexo passando por todas as fases sem copiar código cego.

💾 **O SAVE GAME OBRIGATÓRIO FINAL:**
```bash
git add .
git commit -m "Passo 4: Matriz 3x3 gerada no centro da mesa. Layout concluído!"
git push
```

*(Agora sim! Envie tudo para o GitHub e comemore).*

---

## 🚨 BÍBLIA DE ERROS (TROUBLESHOOTING GRID)

### 🐛 ERRO 1: A Mesa Esmagada (Tudo virou uma tripa)
**O que acontece:** Você criou as 9 divs da mesa, mas em vez de virar um quadrado, elas esmagaram umas as outras em uma única linha.
**A Causa:** Você esqueceu de usar o `display: grid` na classe PAI (`.tabuleiro`). O HTML não adivinha que 9 divs devem virar uma matriz se você não ligar a regra do Grid.
**A Solução:** Vá no CSS e garanta que `.tabuleiro` tem o `display: grid` e o `grid-template-columns: repeat(3, 1fr)`.
