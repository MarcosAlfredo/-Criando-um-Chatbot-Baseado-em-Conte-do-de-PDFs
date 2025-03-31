# Criando-um-Chatbot-Baseado-em-Conte-do-de-PDFs

Cenário
Imagine que você é um estudante de Engenharia de Software, prestes a escrever seu Trabalho de Conclusão de Curso (TCC). Para isso, você precisa revisar e correlacionar diversos artigos científicos. Entretanto, à medida que acumula mais documentos, torna-se cada vez mais difícil extrair informações relevantes e conectar ideias entre diferentes textos.

Diante desse desafio, você decide utilizar inteligência artificial para facilitar esse processo, criando um sistema de busca inteligente capaz de interpretar os PDFs, organizar informações e gerar respostas relevantes com base no conteúdo carregado.

Objetivo
O objetivo deste projeto é permitir que você:

✅ Carregue arquivos PDF contendo informações relevantes para seu estudo ou projeto.
✅ Implemente um sistema de busca vetorial para indexar e recuperar informações dos PDFs.
✅ Utilize inteligência artificial para gerar respostas baseadas no conteúdo dos documentos carregados.
✅ Desenvolva um chat interativo onde seja possível realizar perguntas e obter respostas contextuais fundamentadas nos arquivos.

Explicando algumas functions:

Extração e Indexação dos PDFs:
A função extract_text_from_pdf lê e extrai o texto de cada página dos PDFs encontrados na pasta inputs.
A função load_pdfs_from_directory carrega todos os PDFs do diretório e cria um dicionário com os textos.
O embedding de cada documento é gerado por get_embedding e armazenado com o documento no índice vetorial criado por build_vector_index.

Busca Vetorial e Geração de Respostas:
A função search_query calcula a similaridade entre a consulta do usuário e os embeddings dos documentos para encontrar os mais relevantes.
Com os documentos mais relevantes, a função generate_answer constrói um prompt com o contexto e a pergunta do usuário e chama o Azure OpenAI para gerar uma resposta.

Interface Interativa Aprimorada:
A biblioteca Rich é utilizada para exibir um banner inicial, mensagens coloridas e painéis formatados.
A função run_chatbot implementa um loop interativo onde o usuário envia perguntas e recebe as respostas fundamentadas.
