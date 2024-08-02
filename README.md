# DESAFIO_BEEDOO

## Nesse desafio, realizei uma análise de teste do módulo de cursos da plataforma Beedoo. O objetivo foi identificar possíveis sucessos e erros no produto, visando melhorar a experiência do usuário e a eficácia do sistema

### Cénario e Casos de teste: 
[Clique aqui!](https://docs.google.com/document/d/19bZz5iTxfu6EJ5RrCF1VmunuJcPz9i81JsOPIvXtNS0/edit?usp=sharing)


### Teste em MP4:
[Clique aqui!](https://drive.google.com/drive/folders/1drIlbXKmss2PtilnLMiCiW6e9rG64WTS?usp=drive_link)

---

### Tomei a liberdade de implantar esse desafio no Propio 'Notion', onde criei um documento mais oraganizado e prático para facilitar o processo:
[Clique aqui!](https://imminent-dish-f5a.notion.site/Beedoo-QA-Chalenge-dcce99c9e99d45c297b19a90bcf2d28d?pvs=4)

---

# Relatórios de Bugs

**Metodologia Utilizada: Teste de Software Baseado em Riscos (Risk-Based Testing)**

**Justificativa da Escolha:**
A metodologia de Teste de Software Baseado em Riscos é adequada porque permite focar em áreas do sistema que apresentam maior probabilidade de falhas e que, se falharem, podem causar um impacto significativo. Isso é particularmente útil em ambientes onde recursos são limitados e o tempo é um fator crítico.

### ⚠️**Cenário 2 -**

- **Descrição:** A página de criação de cursos permite a submissão sem preencher campos obrigatórios.
- **Gravidade:** Média
- **Prioridade:** Média
- **Passos para Reproduzir:**
    1. Acessar a página de criação de cursos.
    2. Deixar os campos obrigatórios em branco.
    3. Tentar criar um novo curso.
- **Resultado Esperado:** O sistema deve alertar sobre os campos obrigatórios não preenchidos.
- **Resultado Atual:** O curso é criado sem os dados obrigatórios.

---

### ⚠️Cenário 3 -

- **Descrição:** Validar Campo “Nome do Curso” sem limites de caracteres.
- **Gravidade:** Média
- **Prioridade:** Alta
- **Passos para Reproduzir:**
    1. Acessar a página de criação de cursos.
    2. Inserir um nome de curso com mais de 255 caracteres.
    3. Tentar criar o curso.
- **Resultado Esperado:** O sistema deve limitar o campo "Nome do Curso" a um número razoável de caracteres (ex: 255 caracteres).
- **Resultado Atual:** O sistema permite a criação de um curso com um nome extremamente longo, resultando em possíveis problemas de exibição e armazenamento.

---

### ⚠️ Cenário 4 -

- **Descrição:** Usuário tenta cadastrar um curso com uma data de início no passado.
- **Gravidade:** Média
- **Prioridade:** Alta
- **Passos para Reproduzir:**
    1. Acessar a página de criação de cursos.
    2. Inserir uma data de início que já passou.
    3. Tentar criar o curso.
- **Resultado Esperado:** O sistema deve alertar o usuário que a data de início não pode ser no passado e solicitar uma nova data.
- **Resultado Atual:** O sistema permite a criação do curso com uma data de início no passado, o que pode causar confusão e problemas de planejamento.

---

### ⚠️ Cenário 5 -

- **Descrição:** Usuário não consegue excluir nenhum curso da lista, aparece o erro 405.
- **Gravidade:** Alta
- **Prioridade:** Alta
- **Passos para Reproduzir:**
    1. Acessar a lista de cursos cadastrados.
    2. Tentar excluir qualquer curso da lista.
    3. Observar a mensagem de erro exibida (Erro 405).
- **Resultado Esperado:** O curso deve ser excluído com sucesso, e uma mensagem de confirmação deve ser exibida.
- **Resultado Atual:** O sistema exibe o erro 405 e o curso não é excluído.

