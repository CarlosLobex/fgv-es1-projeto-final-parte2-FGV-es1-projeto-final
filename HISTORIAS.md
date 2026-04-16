# Histórias de Usuário — ESM Forum

---

## Priorização

As histórias foram ordenadas com base em três critérios:

1. **Valor imediato para o usuário** — quanto a funcionalidade melhora a experiência do dia a dia
2. **Complexidade técnica** — esforço de implementação no backend e frontend
3. **Dependências** — se outras features dependem desta para funcionar

| Prioridade | História | Justificativa |
|---|---|---|
| 🥇 1 | Busca por palavra-chave | Maior utilidade imediata; independente de outras features; menor complexidade técnica |
| 🥈 2 | Categorização por tags | Organiza o conteúdo do fórum; impacto positivo na busca futura; complexidade intermediária |
| 🥉 3 | Sistema de votação | Alto valor de engajamento; requer ajustes no modelo de dados e controle de estado |

---

## História 1: Busca de Perguntas por Palavra-Chave

**Como** usuário do fórum,
**Eu quero** buscar perguntas por palavra-chave,
**Para** encontrar rapidamente discussões relevantes sem precisar rolar toda a lista de perguntas.

**Critérios de Aceitação:**
- [ ] A interface deve exibir um campo de busca visível na página principal
- [ ] A busca deve filtrar perguntas cujo título ou corpo contenham a palavra-chave informada (sem distinção de maiúsculas/minúsculas)
- [ ] Os resultados devem ser exibidos em tempo real ou após o envio do formulário de busca
- [ ] Se nenhuma pergunta for encontrada, o sistema deve exibir a mensagem "Nenhuma pergunta encontrada para sua busca"
- [ ] O campo de busca vazio deve restaurar a listagem completa de perguntas

---

## História 2: Categorização de Perguntas por Tags

**Como** usuário do fórum,
**Eu quero** categorizar perguntas com tags (ex: tecnologia, carreira, dúvidas-gerais),
**Para** organizar o conteúdo do fórum e facilitar a navegação por temas de interesse.

**Critérios de Aceitação:**
- [ ] Ao criar uma pergunta, o usuário deve poder selecionar ou digitar uma ou mais tags
- [ ] As tags devem ser exibidas visivelmente em cada pergunta na listagem e na página de detalhes
- [ ] Deve existir uma forma de filtrar perguntas por tag (ex: clicar na tag exibe apenas perguntas daquela categoria)
- [ ] O sistema deve oferecer sugestões de tags predefinidas: `tecnologia`, `carreira`, `dúvidas-gerais`, `outros`
- [ ] Uma pergunta pode ter no máximo 3 tags associadas

---

## História 3: Sistema de Votação em Perguntas

**Como** usuário do fórum,
**Eu quero** votar em perguntas com upvote ou downvote,
**Para** destacar as perguntas mais úteis e relevantes para a comunidade.

**Critérios de Aceitação:**
- [ ] Cada pergunta deve exibir botões distintos de upvote (👍) e downvote (👎) com o contador de votos
- [ ] O contador deve ser atualizado imediatamente após o voto sem recarregar a página
- [ ] Um mesmo usuário não pode votar mais de uma vez na mesma pergunta na mesma direção
- [ ] O usuário pode mudar seu voto (de upvote para downvote e vice-versa); o sistema deve ajustar o contador corretamente
- [ ] A pontuação total da pergunta (upvotes − downvotes) deve ser exibida em destaque

---

*Documento preparado para o Projeto Final de Engenharia de Software — Parte 2.*
