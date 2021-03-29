# spring-boot-basic-microservice
![Java](https://img.shields.io/badge/-Java-0a0a0a?style=for-the-badge&logo=Java) ![Spring](https://img.shields.io/badge/-Spring-0a0a0a?style=for-the-badge&logo=Spring)
<br/>

This is a simple microservice architecture for converting and pricing currencies, built with Spring Boot and Spring Cloud.
It consists of two microservices:
* Forex Service - FS for short
* Currency Conversion Service - CCS for short
<br/>

![Microservices](https://github.com/Mark1708/spring-boot-basic-microservice/blob/main/assets/microservices.png?raw=true)

It uses tape to distribute the load between multiple instances of the Forex service, and Eureka as the name server. If you launch new instances of the Forex service, you can see that the load is automatically distributed between them.
![Deployment](https://github.com/Mark1708/spring-boot-basic-microservice/blob/main/assets/deployment.png?raw=true)
![Eureka](https://github.com/Mark1708/spring-boot-basic-microservice/blob/main/assets/eureka.png?raw=true)
<br/>
<br/>
## Request 1
`GET to http://localhost:8100/currency-converter-feign/from/EUR/to/INR/quantity/10000`
```
{
  id: 10002,
  from: "EUR",
  to: "INR",
  conversionMultiple: 75,
  quantity: 10000,
  totalCalculatedAmount: 750000,
  port: 8000,
}
```
## Request 2
`GET to http://localhost:8100/currency-converter-feign/from/EUR/to/INR/quantity/10000`
```
{
  id: 10002,
  from: "EUR",
  to: "INR",
  conversionMultiple: 75,
  quantity: 10000,
  totalCalculatedAmount: 750000,
  port: 8001,
}
```

<br/>

![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=mark1708&repo=spring-boot-basic-microservice&theme=chartreuse-dark&show_icons=true)
