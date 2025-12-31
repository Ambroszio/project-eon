# 🧪 MVP Técnico - Project Eon

> Este documento define o **MVP técnico inicial** do Project Eon.
> O objetivo do MVP é **validar a arquitetura MMO**, não entregar conteúdo final ou polimento visual.

---

## 🎯 Objetivo do MVP

O MVP técnico deve provar que:

* Cliente e servidor se comunicam corretamente
* Progressão de personagem funciona
* Skills evoluem por uso
* Craft e combate coexistem no mesmo loop
* Persistência de dados é confiável

Se esses pontos funcionarem, o projeto é **tecnicamente viável**.

---

## ⚙️ Stack Inicial

> Stack inicial sugerida - pode ser ajustada pela equipe.

* **Cliente:** GameMaker Studio 2
* **Servidor:** Node.js
* **Comunicação:** WebSockets
* **Persistência:** JSON ou banco simples

---

## 🎮 Cliente (GameMaker Studio 2)

### 1️⃣ Movimento e Estado do Jogador

* Movimento 2D básico
* Sincronização com o servidor:

  * Posição
  * Direção
  * HP
  * Classe (fixa no MVP)

---

### 2️⃣ Classe Inicial

* **Guerreiro** (única classe no MVP)

Motivo:

* Simplicidade
* Validação do combate corpo a corpo

---

### 3️⃣ Combate Básico

* 1 skill ativa: **Ataque Corpo a Corpo**
* Ataque validado pelo servidor
* Dano simples

#### Progressão

* Uso da skill concede XP da skill
* Matar criaturas concede XP de personagem
* Skill limitada pelo nível do personagem

---

## 🌍 Mundo do MVP

* 1 mapa pequeno
* 1 área segura
* 1 área perigosa
* 1 tipo de criatura hostil

O foco é validação, não variedade.

---

## 🔨 Craft (Escopo Mínimo)

### Profissão Disponível

* **Mineração**

### Fluxo

1. Jogador coleta minério
2. Jogador recebe 1 pedido de craft
3. Jogador entrega o pedido
4. Jogador recebe:

   * XP de personagem
   * Gold

> Craftar concede apenas XP da profissão.

---

## 🧾 Sistema de Pedido (Simplificado)

* Pedido único
* Item simples
* NPC fixo

O sistema existe apenas para validar o loop de craft.

---

## 🖥️ Servidor

### Funcionalidades Obrigatórias

* Login simples
* Sessão de jogador
* Gerenciamento de conexões
* Sincronização de posição
* Validação de combate
* Cálculo de XP e skills
* Sistema básico de pedidos

---

## 💾 Persistência de Dados

Salvar no servidor:

* Nível do personagem
* XP do personagem
* Skill de combate
* Skill de mineração
* Gold

Persistência deve ocorrer:

* Logout
* Intervalos regulares

---

## 🔁 Loop Completo do MVP

1. Jogador entra no jogo
2. Move-se pelo mapa
3. Enfrenta criatura
4. Ganha XP de combate
5. Evolui skill por uso
6. Coleta minério
7. Entrega pedido
8. Ganha XP de personagem + gold
9. Dados são salvos

---

## 🚫 Fora do Escopo do MVP

* PvP
* Múltiplas classes
* Sistema de guildas
* Economia avançada
* UI final
* Balanceamento

---

## ⏱️ Estimativa de Desenvolvimento

> Considerando equipe de 3 pessoas (hobby sério).

* Base cliente: 2–3 semanas
* Base servidor: 2–3 semanas
* Combate: 1 semana
* Craft: 1 semana
* Persistência e testes: 1 semana

**Total estimado:** ~6–8 semanas

---

## 📌 Observação Final

Este MVP representa a **fundação técnica do Project Eon**.

Somente após a validação deste MVP o projeto deve expandir em conteúdo, sistemas avançados e polimento visual.
