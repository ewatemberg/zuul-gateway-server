# Zuul Gateway Server
Para crear nuestro servicio Eureka necesitamos una clase Java que contenga toda la funcionalidad necesaria para permitir registrar microservicios. Para ello los creadores de Spring Cloud y Netflix a través de su plataforma OSS nos proporciona la anotación @EnableEurekaServer.
Como base utilizaremos una aplicación Boot con un archivo de entrada (ApplicationEurekaServer.java), que estará anotado con @SpringBootApplication y con @EnableEurekaServer, además de definir una función main que arrancará el servicio. Para ello procederemos de la siguiente manera:

```
package com.example.microservices.gateway.zuulgatewayserver;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;
import org.springframework.cloud.netflix.zuul.EnableZuulProxy;

@EnableDiscoveryClient
@EnableZuulProxy
@SpringBootApplication
public class ZuulGatewayServerApplication {

    public static void main(String[] args) {
        SpringApplication.run(ZuulGatewayServerApplication.class, args);
    }

}
```
Toda la configuración asociada a nuestro gateway la encontraremos en nuestro [Repo](https://github.com/ewatemberg/spring-cloud-configuration-repository)

![alt text](https://raw.githubusercontent.com/ewatemberg/zuul-gateway-server/master/doc/img/repo.jpg)

![alt text](https://raw.githubusercontent.com/ewatemberg/zuul-gateway-server/master/doc/img/java-microservices-with-netflix-oss-spring.jpg)

### Related
* [Spring Cloud Config](https://github.com/ewatemberg/spring-cloud-configuration-server-example)
* [Repositorio Configuración Centralizada](https://github.com/ewatemberg/spring-cloud-configuration-repository)
* [Servicio de Registro y Descubrimiento basado en Eureka](https://github.com/ewatemberg/eureka-discovery-server)
* [Microservicio Echo](https://github.com/ewatemberg/eureka-client-microservice)

#### Fuente:
[Miguel Doctor Yuste](https://medium.com/@migueldoctor/spring-cloud-series-crea-un-servicio-de-registro-y-descubrimiento-con-spring-cloud-netflix-eureka-4758615ad4cb)

