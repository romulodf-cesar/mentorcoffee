# Projeto AulaRAG
Este projeto demonstra a construção de uma aplicação de **RAG (Retrieval-Augmented Generation)**. A abordagem combina busca semântica em documentos com um modelo de linguagem, permitindo gerar respostas baseadas em uma base de conhecimento própria e reduzir respostas imprecisas.

## Como funciona

1. **Ingestão:** os documentos são carregados e divididos em trechos menores (*chunks*).
2. **Embeddings:** cada trecho é convertido em um vetor numérico que representa seu significado.
3. **Indexação:** os vetores são armazenados em um banco vetorial para permitir buscas por similaridade.
4. **Recuperação:** a pergunta do usuário também é convertida em embedding, e os trechos mais relevantes são localizados.
5. **Geração:** os trechos recuperados são enviados como contexto ao modelo de linguagem, que formula a resposta.

## Tecnologias utilizadas

- **Python:** linguagem principal da aplicação.
- **LangChain:** integração entre documentos, embeddings, recuperação e modelos de linguagem.
- **Modelos de linguagem (LLM):** geração das respostas com base no contexto recuperado.
- **Embeddings:** representação semântica dos documentos e das perguntas.
- **Banco de dados vetorial:** armazenamento e busca eficiente dos embeddings.
- **Jupyter Notebook:** exploração, testes e demonstração do fluxo de RAG.

## Benefícios

- Respostas fundamentadas nos documentos fornecidos.
- Atualização da base de conhecimento sem necessidade de treinar novamente o modelo.
- Busca por significado, e não apenas por palavras-chave.
- Separação entre recuperação de informação e geração de texto.

## Fluxo resumido

```text
Documentos → Chunks → Embeddings → Banco vetorial
									  ↑
Pergunta → Embedding → Busca semântica → Contexto + LLM → Resposta
```

## Como executar

1. Instale as dependências do projeto.
2. Configure as credenciais da API do modelo de linguagem, quando necessário.
3. Adicione os documentos à base de conhecimento.
4. Execute o notebook ou a aplicação para realizar perguntas aos documentos.

## Observação

A qualidade das respostas depende da qualidade dos documentos, da divisão dos trechos, do modelo de embeddings e da configuração do mecanismo de recuperação.

## Dicas para Push

- git init
- git status
- git add .
- git commit -m "mensagem"
- git status
- crie um repositório no github
- git remote
- git remote add origin << seu endereço  >>
- git push
