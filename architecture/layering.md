# Camadas

É uma das técnicas mais comuns utilizadas por designers de software1 para quebrar partes de 
um software complicado.

Ao pensarmos em um sistema em termos de camadas, você imagina um subsistema de software organizado 
em algumas camadas, onde cada camada repousa sobre a camada inferior. Neste esquema a camada superior
usa vários serviços definidos na camada inferior, mas a camada inferior não tem conhecimento da camada superior. 
Além disso, cada camada normalmente escode suas camadas inferiores da camada acima, então a camada 4 usa os serviços
definidos na camada 3, que usa os serviços da camada 2, mas a camada 4 não tem conhecimento da camada 2.

Quebrar um sistema em camadas tem vários benefícios:

- Você pode entender uma única camada como um todo coerente sem saber sobre as outras camadas.

- Você pode substituir camadas com uma implementação alternativa.

- Você minimiza a dependência entre camadas.

- Camadas são bons lugares para padronização.

- Depois de criar uma camada, você pode usá-la para muitos serviços de nível superior.

Camadas é um técnica boa, mas há desvantagens.

- Camadas encapsulam bem algumas coisas, mas não todas. Como resultado, às vezes
  você obtém alterações em cascata.

- Camadas extras podem prejudicar o desempenho.

Mas a parte mais difícil de uma arquitetura em camadas é decidir quais camadas ter e
qual a responsabilidade de cada camada.

## As Três Principais Camadas

Aqui estou centralizando minha discução em torno de uma arquitetura de três camadas:

- Apresentação
- Domínio
- Fonte de Dados

A camada de domínio lida com as regras de negócio.
  
A camada de apresentação lida com interações entre o usuário e o software. As responsabilidades
principais da camada de apresentação é mostrar informações e interpretar comandos do usuário
em ações no domínio e na fonte de dados.

A camada de fonte de dados lida com a comunicação com outros sistemas que realizam tarefas em nome da
aplicação. Estes podem ser monitores de transações, outras aplicações, sistemas de mensagens e assim
por diante.
