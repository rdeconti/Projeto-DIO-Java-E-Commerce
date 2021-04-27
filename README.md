:spiral_calendar: Atualizado em 27 de abril de 2021 :heart:

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/Digital%20Innovation%20One%20-%20Logotipo.png" />

# Projeto Digital Innovation One Java

# Criando uma solução de e-commerce com microsserviços em Java
- Este projeto foi proposto pela Digital Innovation One 
- Link do código original: https://github.com/hatanakadaniel/ecommerce-payment-api e https://github.com/hatanakadaniel/ecommerce-checkout-api
- Professor: Daniel Hatanaka
- Aulas: https://web.digitalinnovation.one/lab/criando-uma-solucao-de-e-commerce-com-microsservicos-em-java/learning/506c1caf-2543-42cf-91f7-f4e28f2657ab

# Descrição
Neste projeto prático iremos desenvolver uma solução de e-commerce com a arquitetura de microsserviços e aplicar a integração entre eles orientada a eventos com Apache Kafka e garantir a compatibilidade entre da comunicação dos microsserviços com Schema Registry. Para isso, programaremos em Java utilizando a stack do Spring (Spring Boot, Spring Cloud Streams).

# Detalhes da aula
- Definição dos domínios
    - <img src=”https://github.com/rdeconti/Projeto-DIO-Java-E-Commerce/blob/main/Screens-project/dominios.jpg" />
- Definição da arquitetura
    - https://github.com/rdeconti/Projeto-DIO-Java-E-Commerce/blob/main/Screens-project/arquitetura.jpg
      - checkout Front End realizado com HTML (layout pronto do Spring Boot)
      - checkout Api recebe todos os dados digitados no front end
      - payament Api recebe dados da checkout api e processa o pagamento
      - checkout Api recebe retorno da payament Api e devolve o resultado para usuário no Front End
    - KAFTA trata dados em forma de Streaming Data e utilizando Schema Registry
      - <img src=”https://github.com/rdeconti/Projeto-DIO-Java-E-Commerce/blob/main/Screens-project/apacheKafka.jpg" />
      - <img src=”https://github.com/rdeconti/Projeto-DIO-Java-E-Commerce/blob/main/Screens-project/schemaRegistry.jpg" />
- Spring utilizado com as opções: Boot, Cloud stream, Sleuth e Web    
- Banco de dados Postgres definido para Manter dados das Apis (ver em docker-compose.yml)

# Dependências
- org.springframework.boot:spring-boot-starter-web
- org.springframework.cloud:spring-cloud-starter-sleuth
- org.springframework.cloud:spring-cloud-starter-stream-kafka
- io.confluent:kafka-avro-serializer:5.5.0
- org.projectlombok:lombok

# Exemplos de telas

## Tela inicial



## Tela de acerto

<img src="https://github.com/rdeconti/Projeto-DIO-Java-Gerenciador-De-Pessoas
/blob/main/Test-screens/Tela%20acertou.jpg" />

## Tela de erro

<img src="https://github.com/rdeconti/Projeto-DIO-Java-Gerenciador-De-Pessoas
/blob/main/Test-screens/Tela%20errou.jpg" />
