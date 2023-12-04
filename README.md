 # Api REST e RESTFul

   <p>Uma API REST, ao seguir os princípios da arquitetura REST, amplia suas interações para além do ambiente web, criando uma forma eficaz de comunicação entre clientes e servidores. Ao abraçar esses princípios, a API busca garantir uma transferência suave e estruturada de informações. Essa abordagem envolve conceitos essenciais, como a clara definição de recursos, identificados por URIs, e a transmissão de dados por meio de representações, geralmente em formatos como JSON ou XML. A aplicação consistente de métodos HTTP, tais como GET, POST, PUT e DELETE, guia operações específicas, estabelecendo assim serviços web eficientes.</p>
    
<p>Quando uma API adere integralmente a esses elementos, ela é categorizada como RESTful, refletindo uma implementação que adere aos princípios orientadores da arquitetura REST.</p>
 
## Diferenças entre REST e RESTFul


### REST -  Refere-se aos princípios teóricos e fundamentais da arquitetura.
- Nível de abstração:Refere-se a um estilo arquitetural de alto nível, fornecendo diretrizes gerais para o design de sistemas distribuídos.
- Flexibilidade:Oferece maior flexibilidade ao projetista, permitindo escolhas de implementação mais livres.
- identificação de recursos:Coloca ênfase na identificação clara de recursos por meio de URIs, mas não define regras estritas sobre como essas URIs devem ser estruturadas.
- Estado do Cliente: É um estilo stateless, o que significa que cada requisição do cliente para o servidor contém toda a informação necessária para entender e processar a requisição.
- Manipulação de Recursos: Não define como os recursos devem ser manipulados, deixando essa decisão para o projetista do sistema.
- Padrões de Mensagens:Permite o uso de diferentes formatos de mensagem, como XML, JSON, HTML, entre outros.
- É um estilo arquitetural que define um conjunto de princípios para projetar serviços web.
- Envolve princípios teóricos que orientam como os recursos são definidos e manipulados em um sistema distribuído.
- Pode ser considerado mais como um conjunto de diretrizes e restrições do que uma implementação específica.

### RESTFul - Descreve implementações específicas que seguem esses princípios.
- Nível de abstração:Representa a implementação concreta dessas diretrizes em um serviço web específico, aplicando os princípios do REST de maneira prática.
- Flexibilidade: Envolve uma abordagem mais orientada por convenções, incentivando práticas consistentes e padronizadas para facilitar a compreensão e a interoperabilidade.
- identificação de recursos:Geralmente segue convenções específicas para a criação de URIs, tornando-as mais previsíveis e semânticas.
- Estado do Cliente:Mantém a statelessness, mas a implementação pode envolver estratégias para gerenciar o estado do cliente, como sessões, quando necessário.
- Manipulação de Recursos:Implementa maneiras específicas de manipular recursos, seguindo as boas práticas do REST.
- Padrões de Mensagens:Geralmente adere a um formato de mensagem específico, como JSON, para promover consistência.
- Refere-se à aplicação efetiva dos princípios REST na implementação de um serviço web.
- Implementa adequadamente conceitos como identificação de recursos, utilização correta dos métodos HTTP e suporte a diferentes representações de recursos.
- O termo "RESTful" é muitas vezes usado para descrever sistemas ou serviços que seguem os princípios do REST.

Diante disso, é notável que um serviço web que é chamado de **RESTful** segue os princípios do **REST**.

  ## HTTP verbs

  <p>Referem-se aos métodos de requisição utilizados no protocolo HTTP (Hypertext Transfer Protocol) para indicar a ação desejada sobre um recurso específico. Cada um desempenha papéis específicos na interação entre clientes e servidores na web. Alguns dos principais HTTP verbs:</p>

- <p>GET<br>
  Utilizado para obter a representação de um recurso específico do servidor.</p>

- <p>POST<br>
   Geralmente utilizado para criar um novo recurso no servidor.</p>
   
- <p>PUT<br>
   Usado para atualizar ou criar um recurso.</p>

- <p>DELETE<br>
    Remove o recurso identificado pela URI.</p>

- <p>HEAD<br>
     Semelhante ao GET, mas útil para verificar metadados sem baixar todo o conteúdo.</p>

- <p>OPTIONS<br>
     Usado para descrever as opções de comunicação disponíveis para um recurso ou servidor.</p>

- <p>CONNECT<br>
     Estabelece uma conexão de túnel com o servidor, geralmente para fins de comunicação segura, como SSL/TLS.</p>

- <p>TRACE<br>
     Realiza um teste loop-back, ajudando na depuração, ao retornar as informações recebidas pelo servidor na requisição.</p>

- <p>PATCH<br>
   Aplica modificações parciais a um recurso. Diferente do PUT, que substitui completamente o recurso, o PATCH faz alterações específicas.</p>

     ## HTTP Status Code
  
<p>São códigos numéricos que indicam o resultado de uma requisição HTTP realizada por um cliente a um servidor. Esses códigos são parte fundamental do protocolo HTTP (Hypertext Transfer Protocol) e são incluídos nas respostas do servidor para comunicar o resultado da requisição ao cliente. Algumas categorias principais de códigos de status HTTP:</p>

- <p>1xx: Informativo<br>
   Indica que a solicitação foi recebida e o processo continua.</p>

- <p>2xx: Sucesso<br>
   Indica que a ação foi recebida, compreendida e aceita com sucesso.<br>
   200 OK: A solicitação foi bem-sucedida. O significado exato do sucesso pode variar dependendo do método de solicitação.<br>
   201 Created: A solicitação foi bem-sucedida e resultou na criação de um novo recurso.<br>
   204 No Content: A solicitação foi bem-sucedida, mas não há conteúdo para enviar no corpo da resposta.<br></p>

- <p>3xx: Redirecionamento<br>
   Indica que outras ações devem ser tomadas para concluir a solicitação.</p>

- <p>4xx: Erro do cliente
   Indica que a solicitação contém sintaxe incorreta ou não pode ser atendida.
   400 Bad Request: A solicitação não pôde ser entendida ou estava faltando parâmetros obrigatórios.<br>
   401 Unauthorized: A solicitação requer autenticação do usuário.<br>
   403 Forbidden: O servidor entendeu a solicitação, mas se recusa a autorizá-la<br>
   404 Not Found: O recurso solicitado não foi encontrado no servidor.<br></p>

- <p>5xx: Erro do servidor
    Indica que o servidor não atendeu a uma solicitação aparentemente válida.
    500 Internal Server Error: O servidor encontrou uma situação inesperada que o impediu de cumprir a solicitação.<br>
    502 Bad Gateway: O servidor, enquanto agindo como um gateway ou proxy, recebeu uma resposta inválida do servidor upstream.<br>
    503 Service Unavailable: O servidor não está pronto para lidar com a solicitação. Geralmente, isso é temporário e pode ser devido a sobrecarga do servidor ou manutenção.<br>
    504 Gateway Timeout: O servidor, enquanto atua como um gateway ou proxy, não recebeu uma resposta oportuna do servidor upstream ou algum outro servidor necessário para completar a solicitação.<br></p>

 ---

 **Autor do resumo:**  Luana Vitória Ribeiro Bernardo - 01565426
 



  

    

    
    
