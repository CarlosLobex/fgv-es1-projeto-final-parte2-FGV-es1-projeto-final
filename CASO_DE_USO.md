# Caso de Uso Detalhado — ESM Forum

---

## Caso de Uso: Buscar Perguntas por Palavra-Chave

**Atores:** Usuário (visitante ou membro do fórum)

---

**Pré-condições:**
- O sistema está disponível e com o backend em execução
- Existe pelo menos uma pergunta cadastrada no banco de dados

---

**Fluxo Principal:**

1. O usuário acessa a página principal do ESM Forum
2. O sistema exibe a lista completa de perguntas ordenadas por data de criação (mais recentes primeiro)
3. O usuário localiza o campo de busca e digita uma palavra-chave
4. O sistema realiza uma consulta no banco de dados filtrando perguntas cujo título ou corpo contém a palavra-chave (sem distinção de maiúsculas/minúsculas)
5. O sistema exibe a lista de perguntas correspondentes ao termo buscado
6. O usuário visualiza os resultados e pode clicar em qualquer pergunta para ver seus detalhes e respostas

---

**Fluxo Alternativo 1: Nenhuma pergunta encontrada**

- 4a. A consulta ao banco de dados não retorna nenhum resultado para a palavra-chave informada
- 4b. O sistema exibe a mensagem: *"Nenhuma pergunta encontrada para sua busca. Tente outros termos."*
- 4c. O campo de busca permanece preenchido para que o usuário possa editar o termo
- 4d. O caso de uso encerra sem exibir a listagem

---

**Fluxo Alternativo 2: Usuário limpa o campo de busca**

- 3a. Após realizar uma busca, o usuário apaga o conteúdo do campo de busca
- 3b. O sistema detecta o campo vazio e recarrega a listagem completa de perguntas
- 3c. Retorna ao passo 2 do fluxo principal

---

**Fluxo Alternativo 3: Erro de comunicação com o servidor**

- 4a. O frontend envia a requisição de busca mas não recebe resposta do backend (timeout ou erro 500)
- 4b. O sistema exibe a mensagem: *"Erro ao realizar a busca. Tente novamente."*
- 4c. A listagem anterior é mantida na tela
- 4d. O caso de uso encerra

---

**Pós-condições:**
- A interface exibe apenas as perguntas que correspondem ao critério de busca informado
- Nenhum dado é modificado no banco de dados (operação somente de leitura)
- O usuário pode iniciar uma nova busca ou navegar normalmente pelo fórum

---

*Documento preparado para o Projeto Final de Engenharia de Software — Parte 2.*
