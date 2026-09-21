# 🚀 Aula 49: Criando uma Planilha do Zero


**Unidade:** Modelo Computacional: Simulação com Planilhas  


**Slide RCO de Referência:** `1_6507___1a_serie_aula_49_2026.pdf`  
**Exercícios RCO de Referência:** `1_6507___1a_serie_exercicios_49_2026.pdf`  

---




---

### 🧩 1. O Problema Prático 


**O Dilema do Cronograma de Viagem de Curitiba para Recife:**  
Lucas e sua equipe estão organizando uma viagem de estudos e turismo de Curitiba para Recife. Eles possuem diversos custos envolvidos: passagem de avião, hospedagem, alimentação e transporte local. Se anotarem tudo em papéis soltos ou mensagens de chat, perderão a conta dos valores, não conseguirão somar os gastos rapidamente e correrão o risco de estourar o orçamento.

Lucas precisa de um modelo computacional estruturado onde consiga organizar categorias, inserir estimativas de preços, visualizar e compartilhar o planejamento em tempo real com os seus colegas de equipe.

**A Pergunta-Chave**  
> *Como Lucas pode criar uma planilha eletrônica em branco no Google Planilhas, identificar corretamente colunas, linhas e células, e configurar o compartilhamento seguro para organizar os custos da viagem Curitiba <> Recife?*

---

### 📖 2. Teoria Fundamentadora Completa


#### 2.1 Visão Geral dos Projetos da Unidade
Nesta unidade de **Modelo Computacional: Simulação com Planilhas**, desenvolveremos dois grandes projetos:
1. **Projeto 1 (Cronograma de Viagem):** Cálculo e organização de custos, estatísticas e visualização de dados em gráficos.
2. **Projeto 2 (Simulação Financeira de Longo Prazo):** Parâmetros de ajustes percentuais sobre salário, reserva financeira e juros compostos ao longo dos anos para simulações de aposentadoria e grandes metas.

#### 2.2 Acesso e Configuração Inicial no Google Planilhas
1. **Acesso com Conta Institucional/Pessoal:** Verificar no canto superior direito da tela o ícone do perfil para garantir que o projeto seja salvo corretamente na nuvem.
2. **Criação de Planilha em Branco:** Selecionar a opção de planilha em branco (notando que o Google Planilhas também possui modelos pré-definidos para usos específicos).
3. **Ajustes de Interface:** Fechar a aba lateral de *Tabelas* (clicando no 'x') e ajustar o Zoom para 200% (ou um nível confortável de leitura).
4. **Nomenclatura Significativa:** Alterar o nome padrão "Planilha sem título" no canto superior esquerdo para um nome representativo, como `Viagem de Curitiba <> Recife`.

#### 2.3 Estrutura Fundamental da Planilha Eletrônica
* **Colunas:** Identificadas por **letras** dispostas na vertical em ordem alfabética ($A, B, C, \dots, Z, AA, \dots$).
* **Linhas:** Identificadas por **números** dispostos na horizontal em ordem sequencial ($1, 2, 3, \dots$).
* **Célula:** A interseção exata entre uma coluna e uma linha. É o espaço fundamental onde os dados (textos, números ou fórmulas) são armazenados.
  * **Notação Padrão:** **Letra da Coluna + Número da Linha** (Exemplo: $A1$, $B2$, $D5$).
  * **Caixa de Nome:** Localizada no canto superior esquerdo (acima da coluna A), exibe a célula ativa selecionada.

#### 2.4 Organização de Dados e Inserção de Linhas
* **Célula A1:** Inserção do Título do Projeto: `Cronograma de viagem curitiba recife`.
* **Inclusão de Linhas Superior:** Clique com o botão direito sobre o número da linha 2 $\rightarrow$ selecionar `+ Inserir 1 linha acima` para criar espaço para os cabeçalhos.
* **Cabeçalhos de Coluna:** 
  * Célula $A2$: `Categoria`
  * Célula $B2$: `Preço`
* **Itens de Despesa (Coluna A):** Passagem de avião, Hospedagem, Alimentação, Transporte.

#### 2.5 Colaboração e Permissões de Compartilhamento
O Google Planilhas permite a colaboração em tempo real via nuvem. Ao clicar no botão **Compartilhar** (canto superior direito):
* **Modos de Acesso Geral:**
  * *Restrito:* Apenas pessoas adicionadas manualmente podem acessar.
  * *Qualquer pessoa com elink:* Disponibiliza a planilha para quem possuir a URL.
* **Níveis de Permissão:**
  1. **Leitor:** Pode apenas visualizar os dados, sem realizar alterações (ideal para planilhas públicas para evitar modificações acidentais).
  2. **Comentador:** Pode visualizar e adicionar comentários/sugestões.
  3. **Editor:** Permissão total para inserir, editar ou remover dados e fórmulas.

---

### 💻 3. Sintaxe Básica & Exemplo Análogo (Consulta Visual)

Veja a estrutura da tabela montada na planilha no Google Planilhas:

| Célula | Conteúdo / Texto | Tipo de Dado |
| :--- | :--- | :--- |
| **A1** | `Cronograma de viagem curitiba recife` | Título do Projeto |
| **A2** | `Categoria` | Cabeçalho da Coluna A |
| **B2** | `Preço` | Cabeçalho da Coluna B |
| **A3** | `Passagem de avião` | Item (Texto) |
| **B3** | `1800` | Preço Estimado (Número/Moeda R$) |
| **A4** | `Hospedagem` | Item (Texto) |
| **B4** | `850` | Preço Estimado (Número/Moeda R$) |
| **A5** | `Alimentação` | Item (Texto) |
| **B5** | `500` | Preço Estimado (Número/Moeda R$) |
| **A6** | `Transporte` | Item (Texto) |
| **B6** | `200` | Preço Estimado (Número/Moeda R$) |

---

### 🛠️ 4. Desafio Ativo 


Como integrante da equipe de planejamento:

1. Acesse o [Google Planilhas](https://sheets.google.com) logado na sua conta institucional.
2. Crie uma **Planilha em Branco** e feche o painel lateral de Tabelas.
3. Renomeie a planilha para `Viagem de Curitiba <> Recife` (ou para um destino de sua preferência).
4. Ajuste o Zoom para **200%**.
5. Na célula **A1**, digite o título da planilha.
6. Digite os itens de viagem na coluna A: `Passagem de avião`, `Hospedagem`, `Alimentação` e `Transporte`.
7. Insira uma nova linha acima da linha 2 e adicione os cabeçalhos `Categoria` na **A2** e `Preço` na **B2**.
8. Faça uma pesquisa rápida na internet por estimativas de valores em reais (R$) para cada item e preencha a coluna B (células B3 a B6).
9. Clique em **Compartilhar**, mude o Acesso Geral para *Qualquer pessoa com o link* na função de **Leitor** e copie o link.

---

### 🧪 5. Teste de Validação (5 Minutos)

1. Verifique se a caixa de nome exibe a célula correta ao clicar em cada item.
2. Confirme se a célula $A2$ contém a palavra `Categoria` e a célula $B2$ contém a palavra `Preço`.
3. Abra uma janela anônima no seu navegador e cole o link copiado para validar se o acesso abre corretamente em modo **Leitor** (apenas visualização).

---

### ❓ 6. Quiz de Fixação 


#### Q1. (Slide RCO - Questão 1) Durante a aula, você aprendeu que as planilhas eletrônicas apresentam dados organizados em uma grade formada por interseções de linhas e colunas. Como são chamadas essas interseções?
- (A) Tabela.
- (B) Célula.
- (C) Fórmula.
- (D) Documento.




#### Q2. (Slide RCO - Questão 2) Complete a localização das células em uma planilha relacionando os pares coluna/linha:
1. Interseção da coluna B com a linha 3 $\rightarrow$ Célula **____**.
2. Selecionando a célula D5, ela está na coluna D e na **____**.
3. A primeira célula da planilha (coluna A, linha 1) é chamada de **____**.

- (A) B3 | linha 5 | A1
- (B) 3B | linha D | 1A
- (C) A1 | linha 3 | B3
- (D) B5 | coluna 3 | A1



#### Q3. (Slide RCO - Questão 3) Sobre a estrutura de uma planilha eletrônica, analise as afirmações como Verdadeiras (V) ou Falsas (F):
- ( ) Em uma planilha, as colunas são identificadas por números e as linhas por letras.
- ( ) Cada interseção entre uma coluna e uma linha forma uma célula, onde os dados são inseridos.
- ( ) A célula A1 está localizada na primeira coluna e na primeira linha da planilha.
- ( ) Para identificar uma célula, utilizamos o formato linha + coluna (exemplo: 2A).

Assinale a sequência correta:
- (A) F - V - V - F
- (B) V - V - F - F
- (C) F - F - V - V
- (D) V - F - F - V




#### Q4. No compartilhamento de planilhas no Google Planilhas, qual perfil de permissão permite que o usuário veja as informações sem ter a capacidade de alterar ou deletar os dados da tabela?
- (A) Editor.
- (B) Comentador.
- (C) Leitor.
- (D) Proprietário.


