# Prueba 1: Diagrama de Red

_Esta prueba consiste en el desarrollo de un diagrama de red de una aplicaci贸n web que soporta cargas variables y alta disponibilidad._

## Resoluci贸n 馃摉

_Para resolverla utilic茅 la documentaci贸n de AWS para conocer los servicios, y ver ejemplos de uso. Eleg铆 usar AWS ya que encontr茅 el siguiente [proyecto](https://aws.amazon.com/es/getting-started/hands-on/deploy-nodejs-web-app/) que cumple con requerimientos pedidos. El cu谩l us茅 como modelo para desarrollar la prueba agregando los microservicios requeridos. Y adem谩s porque AWS asegura facilidad de uso, escalabilidad y desempe帽o y es seguro._


## Diagrama 馃摝

![Diagrama de Red](./network_diagram.png)

_Para realizar el diagrama de la red consider茅 que sean parte de 茅l las siguientes APIs:_

* AWS Elastic Beanstalk: para implementar la aplicaci贸n.
* Amazon DynamoDB: para implementar la base de datos no relacional.
* Amazon RDS: para implementar la base de datos relacional.

## Elastic Beanstalk 鈿欙笍

_Se usa el servicio de Elastic Beanstalk ya que permite manejar aplicaciones y adem谩s ofrece la administraci贸n autom谩tica de escalamiento y balanceo._

* Instancias EC2: en las instancias se implementa el frontend en js y en otra el backend.
* Amazon S3 Bucket: en el bucket se van a guardar todos los c贸digos de la aplicaci贸n web y los logs necesarios.
* Load Balancer: es el encargado de balancear las cargas entre las distintas zonas.
* Auto Scaling: es el encargado de asegurar la alta disponibilidad de la aplicaci贸n agregando automaticamente m谩s instancias EC2 para acomodar la carga de la aplicaci贸n.

## DynamoDB 馃敥

_DynamoDB es el encargado de administrar una base de datos NOSQL y asegura la alta disponibilidad y la escabilidad de tablas en base al trafico._


## Amazon Relational Database Service (RDS) 馃敥

_Amazon RDS es el encargado de administrar una base de datos relacional asegurando los requerimientos._

## Links 

* [Implementar una aplicaci贸n web de Node.js](https://aws.amazon.com/es/getting-started/hands-on/deploy-nodejs-web-app/)
* [Conceptos Webserver](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts-webserver.html)
* [DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)
* [Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)
