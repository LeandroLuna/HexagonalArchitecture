# HexagonalArchitecture

A arquitetura hexagonal, também conhecida como "ports and adapters," é uma abordagem de arquitetura de software que visa separar claramente a complexidade de negócio da complexidade técnica em um sistema de software. A arquitetura é uma abordagem importante para o desenvolvimento de software de alta qualidade.

Principais conceitos dessa arquitetura:

- **Complexidade de Negócio**: A complexidade de negócio é a parte do problema que o software deve resolver para atender às necessidades do usuário ou do domínio em que está inserido. Por exemplo, a complexidade de negócio envolve a tomada de decisões com base nos dados de um cliente, como a taxa de juros a ser aplicada a um empréstimo. Isso é o cerne do que o software deve fazer.

- **Complexidade Técnica**: A complexidade técnica refere-se a como o software é projetado e construído para resolver o problema de negócio. Isso envolve a escolha de tecnologias, a estruturação do código, a arquitetura do sistema e outras decisões técnicas. É a complexidade que os desenvolvedores introduzem no processo de desenvolvimento.

- **Separação de Complexidade**: A arquitetura hexagonal promove a separação clara entre essas duas complexidades. Isso significa que o desenvolvedor deve distinguir entre o que é relacionado ao negócio (complexidade de negócio) e o que é relacionado à implementação técnica (complexidade técnica).

- **Portas e Adaptadores**: A arquitetura hexagonal usa o conceito de "portas" (ports) e "adaptadores" (adapters) para implementar essa separação. As "portas" representam as interfaces de entrada e saída do sistema, que definem como o sistema interage com o mundo externo. Os "adaptadores" são responsáveis por conectar as portas ao sistema interno, transformando as chamadas externas em ações internas e vice-versa.

- **Flexibilidade e Manutenção**: Essa arquitetura facilita a manutenção e a evolução do software, pois, ao manter a complexidade técnica separada da complexidade de negócio, é mais fácil modificar a implementação técnica (por exemplo, mudar o banco de dados, framework, protocolo de comunicação) sem afetar as regras de negócio.

- **Proteção do Negócio**: A separação entre as complexidades técnica e de negócio ajuda a proteger as regras de negócio, garantindo que elas permaneçam coesas e independentes de detalhes técnicos. Isso é importante para que as mudanças técnicas não impactem as regras de negócio.

- **Portabilidade e Reutilização**: Ao manter a complexidade técnica encapsulada, o software se torna mais portátil e reutilizável, pois as mudanças técnicas podem ser feitas em adaptadores sem afetar a lógica de negócios.

## Ciclo de vida de um projeto

O ciclo de vida de um projeto de software segue várias fases de desenvolvimento e evolução. 

Etapas principais:

1. **Fase 1 - Desenvolvimento Inicial:**
   - Escolha do banco de dados.
   - Criação de cadastros e validações.
   - Implementação de autenticação.
   - Desenvolvimento de controladores e views.
   - Implementação de um servidor web.

2. **Fase 2 - Adição de Recursos e APIs:**
   - Adição de regras de negócios.
   - Criação de APIs para parceiros.
   - Introdução de ACL (controle de acesso).
   - Inclusão de recursos de relatórios e logs.

3. **Fase 3 - Melhorias de Hardware e Escala Vertical:**
   - Atualização de hardware para suportar mais carga.
   - Introdução de cache.
   - Consumo de APIs de parceiros.
   - Lidar com regras externas de parceiros.

4. **Fase 4 - Gargalos no Banco de Dados:**
   - Necessidade de mais consultas e relatórios.
   - Introdução de comandos via linha de comando.
   - Manutenção de versões antigas de APIs.
   - Abordagens para escala vertical.

5. **Fase 5 - Escala Horizontal:**
   - Adoção de escala horizontal.
   - Solução para compartilhar sessões entre servidores.
   - Transferência de uploads para a nuvem.
   - Soluções de autoscaling para gerenciar o aumento da carga.

6. **Fase 6 - Introdução de Tecnologias Modernas:**
   - Adoção de GraphQL.
   - Resolução de problemas relacionados a versões diferentes de APIs.
   - Gerenciamento de logs distribuídos.
   - Integração com sistemas externos (por exemplo, CRM).
   - Atualização para tecnologias como React.

7. **Fase 7 - Problemas de Consistência e Containers:**
   - Inconsistência de dados com sistemas externos (por exemplo, CRM).
   - Adoção de tecnologias de contêineres (Docker, Kubernetes).
   - Mudanças no processo de CI/CD para contêineres.
   - Problemas de rastreamento e resiliência em sistemas de microsserviços.

8. **Fase 8 - Microsserviços e Complexidade:**
   - Introdução de microsserviços.
   - Desafios na comunicação entre microsserviços.
   - Aumento de complexidade e custos operacionais.
   - Exploração de soluções de resiliência.

9. **Fase 9 - Kubernetes e Integração com Filas:**
   - Adoção do Kubernetes para gerenciamento de contêineres.
   - Problemas de resiliência com microsserviços.
   - Uso de sistemas de mensageria e filas.
   - Contratação de consultorias para enfrentar desafios técnicos.

10. **Fase 10 - O Futuro Incerto:**
    - A fase final não está especificada, mas implica que os desafios e complexidades continuam a se acumular à medida que o sistema evolui.

Esse ciclo de vida de projeto de software ilustra como as aplicações podem se tornar complexas ao longo do tempo devido a decisões técnicas, novos requisitos e evolução tecnológica. Manter uma arquitetura adequada e uma visão clara do design é essencial para evitar que o sistema se torne difícil de gerenciar e manter. Deve-se pensar na sustentabilidade do software desde o início e manter uma arquitetura clara para evitar que o software se torne "legado" e difícil de manter.

## Reflexões importantes

Existem vários fatores importantes sobre o desenvolvimento de projetos de software e problemas comuns que os desenvolvedores enfrentam. Abaixo, estão algumas das reflexões e pontos de destaque:

- **Visão de Futuro**: ter uma visão de futuro ao iniciar um projeto de software. Muitas vezes, os desenvolvedores negligenciam a escalabilidade do sistema, resultando em problemas futuros. É fundamental pensar em como o sistema pode crescer e se adaptar às necessidades futuras desde o início.

- **Estabelecimento de Limites**: definir limites claros no design e na arquitetura do software é fundamental. Limites ajudam a manter as diferentes partes do sistema separadas, evitando que se tornem excessivamente acopladas. Isso facilita a manutenção e evita problemas de compatibilidade.

- **Troca e Adição de Componentes**: os desenvolvedores devem considerar a possibilidade de trocar ou adicionar componentes no sistema. Ignorar essa possibilidade pode resultar em um sistema altamente acoplado, tornando difícil implementar mudanças e melhorias.

- **Escala Horizontal**: A escalabilidade é um ponto crucial. Quando o sistema precisa ser dimensionado horizontalmente, muitas mudanças técnicas podem ser necessárias, como separar sessões, uploads e logs em servidores diferentes. A ausência de planejamento de escalabilidade pode levar a problemas sérios.

- **Otimizações Frequentes**: é comum acumular dívida técnica ao adicionar novas funcionalidades. No entanto, ter limites claros pode ajudar a gerenciar essa dívida técnica e garantir que ela não se acumule a ponto de prejudicar o sistema.

- **Preparação para Mudanças Bruscas**: Os desenvolvedores devem estar preparados para realizar mudanças bruscas no sistema, como a substituição de componentes ou serviços. A criação de camadas anticorrupção pode ajudar a isolar o impacto dessas mudanças na lógica de negócios.

- **Avaliação do Valor do Software**: É importante questionar se todas as mudanças e investimentos no software estão agregando valor ao projeto. A migração para novas tecnologias, como microsserviços e containers, deve ser avaliada quanto ao seu impacto e benefício real.

- **Impacto no Cliente**: a questão de como as mudanças arquiteturais afetam o cliente. Aumentos de custo ou atrasos podem impactar negativamente a relação com o cliente.

- **Julgamento dos Desenvolvedores Anteriores**: evitar julgamentos precipitados sobre o trabalho de desenvolvedores anteriores. Muitas vezes, os problemas técnicos surgem devido a circunstâncias específicas do projeto e pressões de tempo.

- **Perda Gradual de Qualidade**: problemas de desenvolvimento não ocorrem de repente, mas são acumulados ao longo do tempo. O software se perde gradualmente se a visão de futuro não for mantida e se as boas práticas de design não forem seguidas.

## Arquitetura vs Design

Diferença entre arquitetura e design de software:

- **Arquitetura de Software**: A arquitetura de software é uma estrutura de alto nível que define a organização geral de um sistema de software. Ela se concentra em questões abstratas e conceituais, como a estrutura geral, os componentes do sistema e a forma como eles se relacionam. A arquitetura visa garantir que os atributos de qualidade, restrições de alto nível e os objetivos do negócio sejam atendidos pelo sistema. As decisões arquiteturais são frequentemente relacionadas a aspectos macro do sistema, como escalabilidade, distribuição e interações entre módulos.

- **Design de Software**: O design de software é uma atividade mais detalhada que se concentra na implementação concreta dos componentes do sistema. Ele aborda questões específicas, como a estrutura interna dos módulos, a escolha das bibliotecas e tecnologias a serem usadas, a organização das classes e funções, a nomenclatura de variáveis e métodos, e assim por diante. O design de software está preocupado com como as partes do sistema funcionam juntas e como cada componente realiza suas funções de maneira eficaz. As decisões de design frequentemente envolvem detalhes de implementação, como escolher uma linguagem de programação específica, definir a estrutura de dados e criar algoritmos.

Embora ambas as áreas estejam relacionadas e frequentemente interajam, a principal distinção é que a arquitetura se concentra no "o quê" e no "porquê" do sistema, enquanto o design de software se concentra no "como" da implementação. Ambos desempenham um papel importante no desenvolvimento de software de alta qualidade.

## Definição de Arquitetura Hexagonal

A arquitetura hexagonal, também conhecida como "ports and adapters" (portas e adaptadores), é um modelo arquitetural que visa separar a lógica de negócios de uma aplicação da sua interação com componentes externos, como bancos de dados, sistemas de terceiros, interfaces do usuário e outros serviços. Essa arquitetura é projetada para tornar o código mais flexível, isolado e facilmente testável, promovendo uma clara separação entre a complexidade do negócio e a complexidade técnica.

Principais conceitos da arquitetura hexagonal:

- **Objetivo da Arquitetura Hexagonal**: A principal ideia da arquitetura hexagonal é criar um sistema onde a complexidade do negócio (a lógica específica da aplicação) é o ponto central, enquanto as interações com componentes externos, como bancos de dados e interfaces de usuário, são tratadas como "portas" para a aplicação. Essas "portas" permitem que diferentes adaptadores se conectem à aplicação de maneira flexível.

- **Separação de Complexidades**: A arquitetura hexagonal promove uma clara separação entre a complexidade do negócio e a complexidade técnica. O "coração" da aplicação contém a lógica de negócios, que é protegida de mudanças externas. As complexidades técnicas, como acesso a banco de dados ou interações com sistemas externos, são tratadas como adaptações externas e não impactam diretamente a lógica do negócio.

- **Portas e Adaptadores**: As "portas" representam os pontos de entrada e saída da aplicação. Elas definem contratos ou interfaces que permitem que a aplicação se comunique com o mundo externo. Os "adaptadores" são implementações concretas que fazem a ponte entre as "portas" e os serviços externos. Isso significa que, para acessar um banco de dados, por exemplo, você criaria um adaptador de banco de dados que atende às interfaces definidas pelas "portas."

- **Isolamento e Flexibilidade**: A arquitetura hexagonal permite que você substitua ou adicione adaptadores sem afetar a lógica principal da aplicação. Isso torna a aplicação mais flexível, facilita a manutenção e permite testes unitários mais eficazes, pois as partes de negócios podem ser isoladas dos componentes externos.

- **Clareza na Comunicação**: O uso de "portas" e "adaptadores" cria uma comunicação clara e bem definida entre a aplicação e seus componentes externos. Isso facilita a compreensão do fluxo de dados e a interação com sistemas externos.

## Dinâmica da Arquitetura Hexagonal

A dinâmica da arquitetura hexagonal, também conhecida como "ports and adapters," envolve uma clara separação entre a complexidade do negócio e as interações com componentes externos. 

- **Limites e Proteção**: A arquitetura hexagonal define limites claros para a aplicação, onde a complexidade do negócio reside no centro, e a complexidade técnica (interações com componentes externos) fica fora desse limite. Isso cria uma proteção das regras de negócio da aplicação.

- **Componentização e Desacoplamento**: A aplicação é dividida em componentes claramente definidos, como sistema de logs, cache, upload, banco de dados, comandos, sistemas de filas, protocolos de comunicação, entre outros. Cada um desses componentes pode ser tratado de forma desacoplada, facilitando a substituição ou alteração sem afetar o restante da aplicação.

- **Facilidade para Microsserviços**: A separação clara de componentes facilita a evolução para arquiteturas de microsserviços. Quando você deseja quebrar um sistema monolítico em microsserviços, a arquitetura hexagonal já fornece a estrutura desacoplada necessária.

- **Dependência de Abstrações**: A dinâmica da arquitetura hexagonal segue o Princípio da Inversão de Dependência (Dependency Inversion Principle) dos princípios SOLID. Módulos de alto nível (aplicação) não dependem diretamente de módulos de baixo nível (adaptação), mas ambos dependem de abstrações. Essas abstrações são interfaces ou contratos que não dependem dos detalhes de implementação. Isso minimiza o acoplamento, tornando as partes da aplicação intercambiáveis.

- **Separação Clara entre Clientes e Servidores**: Na representação visual, a aplicação está no centro do hexágono, os clientes (quem deseja acessar a aplicação) estão no lado esquerdo e os serviços externos, como bancos de dados, estão no lado direito. Essa divisão clara evita que os clientes ou serviços externos se acoplem diretamente à aplicação.

- **Interfaces e Adaptações**: Para permitir a comunicação entre a aplicação e os clientes ou serviços externos, são definidas interfaces (portas) que funcionam como contratos. Os adaptadores são as implementações concretas que se conectam a essas interfaces. Isso permite que diferentes adaptadores sejam usados sem afetar a aplicação central.

- **Uso de Princípios SOLID**: A aplicação de princípios SOLID, em particular o Princípio da Inversão de Dependência, é fundamental para manter o baixo acoplamento e a flexibilidade na arquitetura hexagonal.

- **Maior Clareza e Flexibilidade**: A arquitetura hexagonal cria uma clara separação entre a lógica de negócios da aplicação e sua interação com o mundo externo. Isso torna o código mais claro, mais facilmente testável e mais adaptável a mudanças.

No geral, a dinâmica da arquitetura hexagonal visa criar um software com limites claros entre as partes do sistema, promovendo um alto grau de desacoplamento e permitindo que diferentes componentes se conectem sem afetar o núcleo da aplicação. Essa abordagem facilita a manutenção, a escalabilidade e a evolução de sistemas de software complexos.

## Hexagonal vs Clean vs Onion

A arquitetura hexagonal, clean architecture e onion architecture compartilham o princípio fundamental de separar a complexidade do negócio do software das interações com componentes externos. No entanto, eles têm abordagens diferentes para alcançar esse princípio.

- **Arquitetura Hexagonal (Ports and Adapters)**:
   - A ênfase principal da arquitetura hexagonal está no conceito de criar um limite claro entre a complexidade do núcleo da aplicação e as partes que interagem com ela.
   - Não impõe uma estrutura específica, como pastas, nomes de arquivos ou camadas. Em vez disso, foca na ideia de adaptadores que conectam o núcleo da aplicação a clientes e componentes externos.
   - A arquitetura hexagonal não dita como você deve organizar as camadas ou módulos em sua aplicação. Você tem liberdade para decidir como dividir e nomear suas partes.
   
- **Clean Architecture**:
   - A clean architecture é uma abordagem mais detalhada que se baseia no princípio da arquitetura hexagonal, mas fornece diretrizes específicas sobre como organizar a estrutura da aplicação.
   - Define camadas bem definidas, incluindo a camada de domínio (core), camada de aplicação (use cases), camada de interface de usuário (UI) e camada de infraestrutura.
   - Impõe uma estrutura específica que sugere a organização de pastas e a separação de responsabilidades, por exemplo, colocando regras de negócios no núcleo da aplicação e detalhes de interface do usuário e infraestrutura nas camadas externas.
   
- **Onion Architecture**:
   - A onion architecture é uma variante da clean architecture que também se baseia no princípio de separação clara da complexidade do negócio e das interações externas.
   - Organiza a aplicação em "camadas concêntricas" com o núcleo no centro, seguido por camadas intermediárias e finalmente camadas externas. As camadas externas correspondem a componentes externos.
   - Reforça o princípio de que nenhuma camada interna deve depender de uma camada externa. A dependência deve fluir das camadas externas para o centro.

Portanto, a principal diferença entre essas abordagens reside na forma como elas definem a estrutura da aplicação. A arquitetura hexagonal fornece um conceito geral, enquanto a clean architecture e a onion architecture são abordagens mais prescritivas com estruturas específicas.