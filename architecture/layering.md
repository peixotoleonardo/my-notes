# Camadas

Camadas é uma das técnicas mais comuns que designers de software usam
para quebrar parte de um software complicado.

Ao pensarmos em um sistema em termos de camadas, você imagina um
subsistema de software organizado em algumas camadas de bolo, onde
cada camada repousa sobre a camada inferior. Neste esquema a camada superior
usa vários serviços definidos na camada inferior, mas a camada inferior não
tem conhecimento da camada superior. Além disso, cada camada normalmente
escode suas camadas inferiores da camada acima, então a camada 4 usa os serviços
definidos na camada 3, que usa os serviços da camada 2, mas a camada 4 não tem
conhecimento da camada 2.

Quebrar um sistema em camadas tem vários benefícios importantes.

- Você pode entender uma única camada como um todo coerente sem saber muito sobre as
  outras camadas.

- Você pode substituir camadas com uma implementação alternativa dos mesmos serviços
  básicos.

- Você minimiza a dependência entre camadas.

- Camadas são bons lugares para padronização.

- Depois de criar uma camada, você pode usá-la para muitos serviços de nível superior.

Camadas é um técnica importa, mas há desvantagens.

- Camadas encapsulam bem algumas coisas, mas não todas. Como resultado, às vezes
  você obtém alterações em cascata.

- Camadas extras pode prejudicar o desempenho.

Mas a parte mais difícil de uma arquitetura em camadas é decidir quais camadas ter e
qual a resonsabilidade de cada camada.