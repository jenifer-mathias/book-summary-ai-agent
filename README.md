# BookSummaryAgent

## Descrição do Projeto
O **BookSummaryAgent** é um agente funcional criado no **Azure Foundry**. Ele recebe um parágrafo de texto (principalmente de livros) e gera várias informações essenciais sobre ele, incluindo:

- **Resumo curto e claro**, mantendo apenas a informação essencial.  
- **Contagem de palavras** do parágrafo original.  
- **Contagem de frases** do parágrafo original.  
- **Tema principal** do parágrafo.  
- **Palavras-chave importantes** (2–3 palavras).

O agente é projetado para trabalhar com qualquer tipo de texto, seja um parágrafo de livro ou uma frase solta, mantendo o comportamento consistente.

## Objetivo
- Resumir textos de forma clara e objetiva.  
- Fornecer informações estruturadas sobre o parágrafo, como contagem de palavras, frases, tema e palavras-chave.

## Fluxo de Criação
1. Criado um **Resource Group** no Azure chamado `leitura-descomplicada-resource-group`. 
<img width="700" height="500" alt="resource-group" src="https://github.com/user-attachments/assets/60dc159c-c11d-4f80-a399-2ae16cd95cbc" />


2. Criado o **BookSummaryAgent** dentro do **Azure Foundry**.  
<img width="700" height="500" alt="book-summary-agent" src="https://github.com/user-attachments/assets/d18642d3-c8ef-4c52-98ab-2176603e9885" />

3. Definidas as **instruções do agente** para gerar resumo, contagem de palavras, contagem de frases, tema e palavras-chave.  

````
Você é um agente que recebe um parágrafo de um livro.
Seu trabalho é gerar:

Resumo curto e claro, mantendo apenas a informação essencial.

Contagem de palavras do parágrafo original.

Contagem de frases do parágrafo original.

Tema principal do parágrafo.

Palavras-chave importantes (2–3 palavras).

Regras:

Não acrescente opiniões.

Não traduza o texto.

Se o parágrafo for muito curto, explique em uma frase.

Retorne apenas no seguinte formato, sem qualquer outra informação:

Resumo: <resumo>
Palavras: <número de palavras>
Frases: <número de frases>
Tema: <tema principal>
Palavras-chave: <palavras-chave>
````

4. Testado com diferentes tipos de textos (parágrafos de livros, frases curtas e textos de exemplo).  
5. Gerado prints da execução do agente.

## Funcionamento:
- O usuário fornece um texto/parágrafo como input.  
- O agente processa o texto e retorna no formato:

````
Resumo: <resumo>
Palavras: <número de palavras>
Frases: <número de frases>
Tema: <tema principal>
Palavras-chave: <palavras-chave>
````

## Prints de Execução
<img width="700" height="500" alt="texto-sol" src="https://github.com/user-attachments/assets/ca968764-01ff-4c6f-8450-5b3c4c267392" />
<br><br>
<img width="700" height="500" alt="texto-revolucao-industrial" src="https://github.com/user-attachments/assets/1d9dd95e-14bb-45b4-be89-4a0816568b8c" />
<br><br>
<img width="700" height="500" alt="frase-choveu" src="https://github.com/user-attachments/assets/cf89e125-1354-49fb-9e2c-4ea1ae97df5d" />
<br><br>
<img width="700" height="500" alt="texto-longo" src="https://github.com/user-attachments/assets/5a7e187a-4274-491a-bd5f-fdd5bac97859" />
<br><br>
<img width="700" height="500" alt="texto-vazio" src="https://github.com/user-attachments/assets/da0f3494-89ee-4a49-9305-f0c416f529fd" />
<br><br>
<img width="700" height="500" alt="texto-caracteres-especiais" src="https://github.com/user-attachments/assets/e402b5b8-9ce6-4923-8b77-01562093bc26" />
<br><br>
<img width="700" height="500" alt="texto-null" src="https://github.com/user-attachments/assets/d38c2d27-af39-4a23-99bb-a8908817e150" />

## Referências
- [Azure Foundry](https://learn.microsoft.com/azure/ai-foundry)  

## Melhorias Futuras
- Integrar o **BookSummaryAgent** em um aplicativo.  
- Utilizar **Azure Cognitive Services** para:  
  - Reconhecimento de texto via imagens da galeria ou fotos tiradas pelo app (OCR).  
  - Tradução automática dos textos reconhecidos para diferentes idiomas.


