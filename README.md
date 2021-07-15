# Projeto com Microservice e Spring Cloud

## Requisitos: 
<li> IntelliJ ou outra IDE java;
<li> Spring Boot Initlzr;
<ul> product-catalog (Spring Boot Actuator; Spring Web; Spring Data Elasticsearch;</ul>
<ul> config-server (Spring Boot Actuator; Spring Web; Config Server);</ul>
<ul> Service Discovery (Eureka Server; Config Client)- Todo serviço que se iniciar ele vai se registrar no Serviço Discovery. Ele quem vai saber quem são os serviços,em que porta está respondendo. Vai intermediar a comunicação entre os serviços como um serviço de "guia" dos serviços.</ul>
<ul> Gateway (Spring Boot Actuator; Gateway; Config Client). </ul>
<li> JDK, Java 8;
<li> <a href="https://www.elastic.co/pt/downloads/elasticsearch">Elasticsearch</a>;
<ul> Elasticsearch permite armazenar, buscar e analisar grandes quantidades de dados estruturados e não estruturados; </ul>
<li> Docker - criar container;
<li> Redis;
<p></p><br/>

## Observações:
<p><b> Para que a aplicação acesse o Elasticsearch, o mesmo deve estar rodando na máquina.</b></p>
<p> Ao criar Microserviços, o ideal é que se evite dependência de outros serviços. Neste caso, o Elasticsearch seria importante para o Microservice. O spring, através do actuator, tem a capacidade de identificar e apontar se o serviço está ou não "healthy" (saudável). 
<p> Levando em consideração que o Elasticsearch seria necessário e com o objetivo de evitar o SPOF - Single Point Of Failure, utilizou-se do Docker para criar clusters.</p><br/>

## Testar actuator e http health:

``` http http://localhost:8080/actuator ```

``` http http://localhost:8080/actuator/health ```

