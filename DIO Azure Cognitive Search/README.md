# DIO_AzureCognitiveSearch
Utilizando AI Search para indexação e consulta de dados

O interessante desse laboratório realmente é ele diversificar e integrar conhecimentos , utilizaremos, o Azure AI Search o Azure AI Service e o Storage Account
Quero enfatizar alguns pontos:
Nesse passo eu já visualizo os arquivos docx com depoimentos de usuários de mídias sociais já predefinidos pelo laboratório no Storage Account.
inputs/Cognitive.jpg

 


O programa nos traz o conceito de blob: (Binary Large OBject) refere-se a um tipo de dado que pode armazenar grandes quantidades de informações de forma binária, como imagens, vídeos, documentos ou qualquer outro tipo de arquivo. Em bancos de dados, por exemplo, um blob é frequentemente usado para armazenar dados binários, como imagens ou arquivos PDF, após o upload ele passa a ser definido sob esse conceito.

inputs/Container.jpg
 
Aqui está uma visão geral de como funciona o index no Azure Search:

1. **Criação do índice**: Para começar a usar o Azure Search, você precisa criar um índice. Um índice é uma coleção de documentos que você deseja tornar pesquisáveis. Você define a estrutura do índice especificando quais campos dos seus documentos devem ser indexados e quais tipos de dados esses campos contêm.

2. **Ingestão de dados**: Depois de criar o índice, você precisa carregar os dados que deseja indexar. Isso pode ser feito por meio de várias fontes de dados, como bancos de dados, armazenamentos de blobs, serviços da web ou mesmo documentos JSON. O Azure Search fornece APIs e bibliotecas para ajudar na ingestão de dados.

3. **Indexação**: Uma vez que os dados são carregados, o Azure Search indexa esses documentos com base na estrutura do índice que você definiu. Durante o processo de indexação, o Azure Search analisa o conteúdo dos documentos e cria um índice invertido, que mapeia termos para os documentos que os contêm. Isso permite uma pesquisa eficiente.

4. **Consulta de pesquisa**: Depois que os documentos são indexados, você pode realizar consultas de pesquisa no Azure Search para recuperar documentos relevantes. Você pode usar consultas simples ou avançadas para pesquisar nos campos indexados, filtrar os resultados e classificá-los conforme necessário.

5. **Manutenção do índice**: O Azure Search oferece recursos para manter e atualizar o índice à medida que seus dados mudam. Isso inclui suporte para indexação incremental, onde apenas os documentos modificados são reindexados, e operações de gerenciamento do esquema do índice, como adicionar novos campos ou modificar configurações existentes.
Em resumo, o "index" no Azure Search é a estrutura de dados que torna possível realizar pesquisas eficientes em grandes conjuntos de documentos. Ele armazena informações sobre os documentos indexados e fornece funcionalidades avançadas de pesquisa, como filtragem, classificação e análise de texto.


 
Nos exemplos temos um documento extraído “estático”, mas pesquisando a fundo percebo um dentre as muitas maneiras de termos uma análise de sentimentos incremental, dentre as formas uma que encontrei é configurar a política de log de um software de mídia social instalado em um VM fazendo a correspondência, e o recurso da nuvem reconhecerá os sentimentos gerados pela rede os requisitará pelo arquivo. Json e a indexação fará essa sincronização automaticamente atualizando os índices.
https://docs.servicenow.com/pt-BR/bundle/vancouver-servicenow-platform/page/product/configuration-management/task/sgc-cmdb-set-azure-policies.html


 
A busca por sentimentos negativos funciona da seguinte forma:
 inputs/Indexdia22.jpg

Neste passo selecionamos o Index e buscamos os depoimentos que foram obtidos por região, no nosso caso a cidade de Chicago. Então ele demonstra as  palavras-chaves, frases-chaves, e sentimentos.
  inputs/Negativo.jpg

