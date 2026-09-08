# Memorando de Decisão — Fonte de Dados do Projeto


| Campo | Informação |
|---|---|
| Curso / Disciplina | Ciências da Computação / Estrutura de Dados II   |
| Projeto Integrador | Preditor de Falha e Risco em Dispositivos de Rede |
| Projeto integrador | Reditor de Falha e Risco em Dispositivos de Rede |
| Orientador(a) | Prof. Andréa Ono Sakai, Prof. Denise Braito de Souza |
| Data de entrega desta etapa                                   | 08/09 |
| Integrantes do grupo | Victor Gabriel Alves, Livia Freixo, Rodrigo Camargo |
---

## 1. Situação

Fase incial: o nosso grupo precisa verificar a API do RIPE Atlas para a coleta de dados de medição ICMP, garantindo que o pipeline receba dados válidos para extração de latência, perda e resposta.

## 2. Opção A — Dataset real

<!-- O que foi encontrado sobre um dataset real de ICMP. Cite a fonte de cada informação. -->

- **Origem / link:** [ Zenodo — Dataset of RTT latency internet measurements in Europe. DOI: 10.5281/zenodo.15944458.  ]
- **Formato:** [CSV, incluindo os arquivos Landmark_RTTfingerprint_dataset.csv e Target_RTTfingerprint_dataset.csv, além de um arquivo README. ]
- **Período coberto:** [27 de novembro de 2024 a 30 de janeiro de 2025. ]
- **Campos disponíveis:** [measure_id, identificador do destino, tipo do destino, endereço IP, horário da medição, código do país, latitude, longitude, intervalos de tempo e estatísticas de latência RTT. ]
- **Licença de uso:** [a página do repositório da Universidad Politécnica de Cartagena identifica o dataset como CC0 1.0, permitindo seu uso sem as restrições de uma licença tradicional de copyright. ]

**Resumo do que foi encontrado:**

[Escreva aqui, citando a fonte consultada]

## 3. Opção B — API do RIPE Atlas

<!-- O que foi encontrado sobre a API: autenticação, criação e consulta de medições. Cite a fonte de cada informação. -->

- **Documentação consultada (link):** RIPE Atlas API v2 Documentation ([https://ripe-atlas-api.readthedocs.io/](https://www.google.com/search?q=https://ripe-atlas-api.readthedocs.io/) e [https://atlas.ripe.net/docs/apis/](https://atlas.ripe.net/docs/apis/))
- **Autenticação exigida:** API Key (Chave de API) enviada via cabeçalho HTTP (`Authorization: Key \<sua-chave\>`) ou parâmetro de URL. Para criar medições, necessário consumir créditos do RIPE Atlas.

- **Como se cria uma medição:** - **Como se cria uma medição:** Envia-se uma requisição HTTP `POST` para o endpoint `/api/v2/measurements/` com um corpo JSON definindo o tipo (`type: "ping"`), os alvos (`target`), o número de pacotes, o intervalo e o tipo de sondas a serem utilizadas.

- **Como se consultam os resultados:** Através de requisição HTTP `GET` no endpoint `/api/v2/measurements/\{id\}/results/`. Os resultados retornam em formato JSON detalhado, contendo arrays com os valores individuais de RTT de cada pacote ICMP enviada por cada sonda.

**Resumo do que foi encontrado:**

[Escreva aqui, citando a fonte consultada]

## 4. Comparação

<!-- Preencha a tabela com base no que você levantou nas seções 2 e 3. -->

| Critério | Opção A — Dataset real | Opção B — API RIPE Atlas |
|---|---|---|
| Controle sobre a coleta | | |
| Diversidade geográfica | | |
| Custo / complexidade de implementação | | |
| Tempo até os primeiros dados estarem disponíveis | | |

## 5. Recomendação

<!-- Uma frase direta: qual opção você recomenda. -->

[Escreva aqui]

## 6. Justificativa

<!-- Por que essa opção vence a outra, com base nas evidências das seções 2, 3 e 4 — não em preferência pessoal. -->

[Escreva aqui]

## 7. Riscos e limitações

<!-- O que pode dar errado com a opção escolhida, e como isso poderia ser mitigado. -->

[Escreva aqui]

## 8. Contribuição Individual dos Integrantes

<!-- cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez nesta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "pesquisei , analisei, testei, ... apresentei prós/contras ao grupo, ...").-->

### Integrante 1 — Victor Gabriel Alves
- **O que fez nesta etapa:** pesquisa e documentação 1(situação), 3(API RIPE Atlas)
- **Tempo dedicado (aprox.):** ex.: 3h00
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*:
`[]` 
`[]`

### Integrante 2 — `[Escreva nome completo do aluno ]`
- **O que fez nesta etapa:** `[]`
- **Tempo dedicado (aprox.):** `[ex.: 3h30]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*:
`[]` 
`[]`

### Integrante 3 — `[Escreva nome completo do aluno ]`
- **O que fez nesta etapa:** `[]`
- **Tempo dedicado (aprox.):** `[ex.: 3h30]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*: 
`[]` 
`[]`

### Integrante 4 — `[Escreva nome completo do aluno ]`
- **O que fez nesta etapa:** `[]`
- **Tempo dedicado (aprox.):** `[ex.: 3h30]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*: 
`[]` 
`[]`

### Integrante 5 — `[Escreva nome completo do aluno ]`
- **O que fez nesta etapa:** `[]`
- **Tempo dedicado (aprox.):** `[ex.: 3h30]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*: 
`[]` 
`[]`

### Integrante 6 — `[Escreva nome completo do aluno ]`
- **O que fez nesta etapa:** `[]`
- **Tempo dedicado (aprox.):** `[ex.: 3h30]`
- **Evidência da contribuição** *(print de conversa, rascunho, e-mail, documento compartilhado etc.)*: 
`[]` 
`[]`

---

## Fontes consultadas

<!-- Mínimo de 3 fontes. Liste todas as páginas de documentação, artigos ou repositórios usados. -->

1. [ ]
2. [ ]
3. [ ]
