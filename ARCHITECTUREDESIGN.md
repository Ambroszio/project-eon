# Architecture Design - Project Eon

> Documento de arquitetura cliente-servidor do Project Eon.
> Define **responsabilidades, fluxos e decisões técnicas** para o MVP e futuras expansões.

---

## 🎯 Objetivo da Arquitetura

A arquitetura do Project Eon foi projetada para:

* Sustentar um MMORPG online 2D
* Garantir progressão confiável e segura
* Evitar cheats e inconsistências
* Permitir expansão futura sem reescrita completa

O foco inicial é **validar a arquitetura no MVP**, não escalar massivamente.

---

## 🔐 Princípio Central - Servidor Autoritário

O **servidor é a única fonte de verdade**.

Isso significa:

* O cliente nunca decide resultados importantes
* Toda progressão é validada no servidor
* Estados críticos são calculados server-side

O cliente apenas:

* Envia intenções
* Renderiza estados
* Exibe feedback visual

---

## 🎮 Cliente (GameMaker Studio 2)

### Responsabilidades

* Capturar input do jogador
* Enviar intenções ao servidor
* Renderizar o mundo
* Exibir UI e feedback visual
* Reproduzir animações

### O Cliente **Não** Faz

* Calcular dano final
* Atualizar XP ou skills
* Validar craft ou combate
* Persistir dados

O cliente deve sempre assumir que o servidor pode **corrigir ou negar** uma ação.

---

## 🖥️ Servidor (Node.js)

### Responsabilidades

* Gerenciar conexões
* Manter o estado verdadeiro do jogo
* Validar movimentação
* Processar combate
* Processar craft e pedidos
* Calcular XP e skills
* Persistir dados

Toda lógica que altera o mundo **vive no servidor**.

---

## 🔁 Comunicação

### Protocolo

* WebSockets
* Mensagens em JSON

### Tipos de Mensagens (MVP)

#### Cliente → Servidor

* `login`
* `move`
* `attack`
* `gather`
* `deliver_order`

#### Servidor → Cliente

* `state_update`
* `combat_result`
* `xp_update`
* `skill_update`
* `error`

---

## 🧠 Estado do Jogador (Servidor)

Cada jogador conectado possui um estado persistido no servidor:

* ID
* Posição
* HP
* Nível
* XP
* Skills de combate
* Skills de craft
* Gold
* Estado atual (idle, combat, gathering)

O cliente apenas **espelha** essas informações.

---

## 🗺️ Mundo e Entidades

### MVP

* Um mapa
* Entidades simples:

  * Jogadores
  * Criaturas
  * Recursos de coleta
  * NPCs

### Futuro

A arquitetura permite:

* Múltiplos mapas
* Instâncias
* Áreas perigosas

Sem necessidade de refatoração estrutural.

---

## 🛡️ Combate

* Totalmente validado no servidor
* Cliente envia apenas a intenção de atacar
* Servidor:

  * Valida alcance
  * Calcula dano
  * Atualiza HP
  * Atualiza XP e skill

Cliente recebe apenas o resultado.

---

## 🔨 Craft e Pedidos

* Coleta validada no servidor
* Pedidos controlados pelo servidor
* Entrega de pedidos concede XP de personagem e gold
* Craft concede XP de profissão

Nenhuma lógica de progressão ocorre no cliente.

---

## 💾 Persistência

### Dados Persistidos

* Progresso do personagem
* Skills
* Gold
* Estado básico

### Momentos de Salvamento

* Logout
* Intervalos regulares
* Eventos críticos (level up)

Formato inicial simples (JSON), com possibilidade de migração futura para banco de dados.

---

## ⏱️ Sincronização

### Movimento

* Cliente envia movimento
* Servidor valida e corrige quando necessário

### Combate e Skills

* Sempre server-side
* Sem predição no MVP

---

## 📈 Escalabilidade (Planejada)

Não implementada no MVP, mas prevista:

* Separação lógica por mapas
* Possibilidade de shards
* Servidores dedicados por região

A arquitetura não bloqueia essas expansões.

---

## 🚫 Fora do Escopo do MVP

* Load balancing
* Anti-cheat avançado
* Migração de dados
* Cloud scaling automático

---

## 📌 Observação Final

Este documento define a **base técnica do Project Eon**.

A partir desta arquitetura, o projeto pode crescer de forma incremental, mantendo consistência, segurança e clareza para toda a equipe.
