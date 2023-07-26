## Production
URL: https://planificapistas-ddd-cqrs.onrender.com/ping
Devuelve "Pong!"

## Sonar status

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=bugs)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=JC-Saldana_planificapistas-ddd-cqrs&metric=coverage)](https://sonarcloud.io/summary/new_code?id=JC-Saldana_planificapistas-ddd-cqrs)

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

# Project requirementes

Vamos a realizar el back-end de un proyecto utilizando DDD y CQRS, implementando al menos 2 casos de uso (1 Command y 1 Query).

Los pre-requisitos en cuanto a conocimiento son:

- Clean Code
- Principios de diseño (SOLID y YAGNI principalmente)
- Patrones de diseño
- Clean Architecture (DDD, CQRS y Event Driven Architecture)
- TypeScript
- Testing con Jest

## Fases del proyecto

El proyecto tendrá las siguientes fases:

1. **Descripción e idea del proyecto (Domingo 23 de Julio)**: Esta fase consiste en definir la idea y en describir tanto el proyecto como la empresa. El formato será en markdown dentro del proyecto con el nombre `IDEA.md`
2. **Definición de los Bounded Context**: En esta fase se definirán los diferentes contextos funcionales del proyecto utilizando el método de **Event Storming**. Se debe entregar en el repo un draw.io o cualquier diagrama donde se especifiquen los diferentes Bounded Context, añadiendolo al readme del proyecto [Cheat Sheet Event Storming](https://github.com/ddd-crew/eventstorming-glossary-cheat-sheet)
3. **Identificación del dominio**: Elegiremos dos bounded Contexts, siendo al menos uno de ellos el que vayamos a implementar y realizaremos un diagrama que añadiremos al README.md del proyecto con los elementos de Dominio identificados (Entidades, Value Objects, Aggregates, Domain Events and repositories abstraction). Además deberemos identificar las validaciones en esta capa

Realizar la implementación del dominio de ambos bounded context en TypeScript.

4. **Identificación de la capa de aplicación**: Identificar los casos de uso de los bounded contexts elegidos en un listado, escrito dentro del README.md del proyecto.

Además crearemos dos **Diagramas de casos de uso**, uno para un Comando y otro para la Query.

Realizar la implementación de estos dos casos de uso. 

**En esta fase todavía no hace falta implementar los repositories o el bus de eventos**, podemos usar las abstracciones

5. **Añadir la capa de infraestructura y adapters**: Implementar los repositorios, event bus y mappers de esta capa.

Los casos de uso deben poder estar disponibles via **REST API** o **GraphQL**

## Stack Tecnológico

Para la implementación debemos usar el siguiente Stack Tecnológico:

- **Github**: Como herramienta de versionado de código y CI/CD (Github Actions)
- **SonarQube**: Como herramienta de calidad de código y clean code. Siempre debemos mantener sonar "limpio" y con un 80% de cobertura, siendo un 100% al final del proyecto
- **Eslint, Prettier y hooks**: Como herramienta de análisis de código y gestión del formato.
- **TypeScript**: Superset del lenguaje de programación de JavaScript. **No debemos tener `any` en nuestra implementación**
- **Express** o **NestJS**: Como librería/framework para la implementación del API REST
- **GraphQL**: Como librería para la implementación del API GraphQL
- **Redis**: Como servidor de cache para la implementación de CQRS. Podéis encontrar un cloud gratuito en el propio redis. Podéis usar otras alternativas que encontréis. [https://redis.com/redis-enterprise-cloud/pricing/](https://redis.com/redis-enterprise-cloud/pricing/]
- **Kaftka** o **RabbitMQ** o **nats**: Para la implementación de un bus de eventos en la implementación de Event Driven Architecture. Buscad un cloud gratuito de instancias. Por ejemplo para kaftka: [https://www.conduktor.io/pricing/](https://www.conduktor.io/pricing/)
- **MongoDB** o otra **SQL Database (PostgreSQL, MySQL, ...)**: Como DDBB, podéis elegir una, otra o ambas. Podéis buscar un cloud gratuito para el servidor, como por ejemplo [Atlas](https://www.mongodb.com/es/atlas/database)
- **bitloops** (OPTIONAL): podéis usar esta librería para la ayuda en la implementación de DDD.

## Entrega

La entrega consistirá en un repositorio de Github con las entregas de documentación, el código, las instrucciones para su ejecución y las URL's de las API's tanto Rest como GraphQL.

A nivel de despliegue podéis entregar también dentro de un repo un Docker Compose para poder levantar el entorno en local.

Se presentará en la graduación el día 15 de Septiembre, donde tendremos una primera parte donde enseñaremos nuestros contextos y dominios y otra segunda parte donde enseñaremos el flujo del comando en código.

El tiempo máximo de presentación serán 20 minutos.

