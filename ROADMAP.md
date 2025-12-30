# 🗺️ ROADMAP — Project Eon

> ⚠️ **Aviso importante**
> As durações indicadas abaixo são **estimativas**, pensadas para uma equipe pequena.
> Este roadmap existe para **dar direção e ordem técnica**, não para impor prazos rígidos.

---

## Visão Geral

**Project Eon** é um MMO 2D de fantasia medieval, com foco em **progressão significativa**, onde **combate e craft possuem peso equivalente** na evolução do personagem.

O desenvolvimento seguirá uma abordagem incremental, garantindo que cada fase entregue algo **jogável e validável**, evitando retrabalho e escopo excessivo.

---

## Estrutura do Roadmap

* Desenvolvimento por fases independentes
* Cada fase possui entregas claras
* Sem datas fixas ou promessas de lançamento
* O escopo pode ser ajustado conforme decisões técnicas da equipe

---

## 🧱 FASE 0 - Preparação & Alinhamento

**Duração estimada:** 2–3 semanas

### Objetivo

Estabelecer uma base técnica e organizacional sólida antes do início do desenvolvimento de gameplay. Também com foco em organizar a equipe.

### Entregas

* Repositório GitHub organizado
* README (pitch do projeto)
* Definição da arquitetura inicial
* Estrutura básica de pastas (cliente e servidor)
* Convenções de código
* Decisão técnica inicial:

  * Cliente: GameMaker Studio 2
  * Servidor: Node.js

📌 *Nenhuma feature de gameplay é implementada nesta fase.*

---

## 🚶 FASE 1 - MVP Técnico Online

**Duração estimada:** 6–8 semanas

### Objetivo

Validar a base multiplayer do projeto.

### Funcionalidades

* Conexão cliente ↔ servidor
* Login simples (ID temporário)
* Spawn de jogadores
* Movimento sincronizado
* Visualização de outros jogadores
* Desconexão segura

### Resultado Esperado

Jogadores conseguem se conectar e andar juntos no mesmo mapa.

📌 *Este é o primeiro grande marco do Project Eon.*

---

## ⚔️ FASE 2 - Combate Online Básico

**Duração estimada:** 6–8 semanas

### Objetivo

Introduzir gameplay ativo e interação com o mundo.

### Funcionalidades

* Sistema de vida
* Ataque básico
* Criaturas controladas pelo servidor
* Cálculo de dano no servidor
* Morte e respawn

### Resultado Esperado

Jogadores enfrentam criaturas de forma cooperativa.

---

## 🎒 FASE 3 - Inventário & Itens

**Duração estimada:** 4–6 semanas

### Objetivo

Criar a base para progressão, craft e economia.

### Funcionalidades

* Inventário persistente
* Tipos de itens:

  * Recursos
  * Equipamentos
  * Consumíveis
* Sistema de drop
* Salvamento de progresso

### Resultado Esperado

Jogadores acumulam progresso persistente.

---

## 🔨 FASE 4 - Sistema de Craft

**Duração estimada:** 6–8 semanas

### Objetivo

Garantir que o craft tenha peso equivalente ao combate na progressão do personagem.

### Funcionalidades

* Profissões de craft iniciais
* Coleta de recursos
* Sistema de receitas
* Bancadas de craft
* Craft concedendo experiência ao personagem
* Progressão possível sem combate obrigatório

### Resultado Esperado

Jogadores conseguem evoluir focando apenas em atividades de craft.

---

## 📈 FASE 5 - Progressão do Personagem

**Duração estimada:** 6–8 semanas

### Objetivo

Unificar combate e craft em um sistema de progressão coerente.

### Funcionalidades

* Sistema de nível do personagem
* Experiência proveniente de:

  * Combate
  * Craft
* Atributos
* Escalonamento de dificuldade
* Curva de progressão balanceada

### Resultado Esperado

Loop completo de progressão funcional e satisfatório.

---

## 🗺️ FASE 6 - Conteúdo & Expansão Controlada

**Duração:** contínua

### Objetivo

Expandir o jogo sem comprometer a estabilidade.

### Possíveis Adições

* Novos mapas (instâncias)
* Novas criaturas
* Novas receitas
* Ajustes de balanceamento
* Testes de carga

### Resultado Esperado

Versão beta fechada estável.

---

## Fora do Escopo Inicial

* PVP
* Guildas
* Mundo aberto massivo
* Sistemas avançados de monetização

Esses elementos podem ser avaliados futuramente, após validação do core do jogo.

---

## Considerações Finais

Este roadmap representa uma **visão inicial estruturada** do Project Eon. Ele pode (e deve) evoluir conforme a equipe cresce, decisões técnicas são tomadas e o projeto amadurece.

📌 O foco principal é **construir algo jogável, sustentável e tecnicamente saudável**.
