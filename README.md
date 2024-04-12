MODIFICACION DE PRUEBA



# microservicios
MICROSERVICIOS CON DOCKER, PHP Y MYSQL
Este es un ejemplo de implementación de microservicios con Docker en AWS.
> 
> Los microservicios en AWS con Docker, PHP y MySQL representan una arquitectura de desarrollo de aplicaciones distribuidas que aprovecha los servicios en la nube de Amazon Web Services (AWS) junto con tecnologías como Docker, PHP y MySQL. Aquí te explico qué implica cada componente:

Microservicios: En lugar de construir una aplicación monolítica, los microservicios dividen una aplicación en pequeños servicios independientes, cada uno enfocado en una tarea específica o función de negocio. Estos servicios se pueden desarrollar, desplegar y escalar de forma independiente. Esto facilita la modularidad, la escalabilidad y la actualización de partes específicas de la aplicación sin afectar al conjunto completo.

AWS (Amazon Web Services): Es una plataforma de servicios en la nube que ofrece una amplia gama de servicios para ayudar a las empresas a desarrollar y ejecutar aplicaciones de manera escalable y segura. AWS proporciona servicios como computación en la nube, almacenamiento, bases de datos, análisis, machine learning, entre otros.








Docker: Es una plataforma de contenedores que permite empaquetar aplicaciones y sus dependencias en contenedores virtualizados y portátiles. Docker facilita la creación, implementación y administración de aplicaciones en entornos de desarrollo y producción, al proporcionar un entorno aislado y consistente en cualquier infraestructura.

PHP: Es un lenguaje de programación ampliamente utilizado en el desarrollo web. Es conocido por su simplicidad y facilidad de uso, así como por su amplia comunidad de desarrolladores y una gran cantidad de frameworks y librerías disponibles para el desarrollo web.

MySQL: Es un sistema de gestión de bases de datos relacional de código abierto ampliamente utilizado en aplicaciones web. Proporciona una base de datos rápida, confiable y escalable que se integra bien con PHP y otras tecnologías web.

Cuando se combinan estos componentes en AWS, se pueden construir arquitecturas de microservicios altamente escalables y flexibles. Por ejemplo, cada microservicio puede ser empaquetado en un contenedor Docker y ejecutado en AWS utilizando servicios como Amazon Elastic Container Service (ECS) o Amazon Elastic Kubernetes Service (EKS). Además, AWS proporciona servicios de base de datos como Amazon RDS (Relational Database Service) que pueden ser utilizados para alojar bases de datos MySQL de manera escalable y administrada. En resumen, los microservicios en AWS con Docker, PHP y MySQL permiten construir aplicaciones modernas que pueden escalar fácilmente para satisfacer las demandas cambiantes del negocio.

PASO 1: Tener cuenta AWS

PASO 2: Instalar Docker Version 3.9

````
sudo yum update -y
sudo yum install -y docker
sudo usermood -a -G docker $(whoami)

````

    
PASO 3: Instalar Docker-compose

#descargarse el binario para utilizar docker-compose
    
````
    
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
````
#dar permisos de ejecucion al archivo binario
````
sudo chmod +x /usr/local/bin/docker-compose

````

#comprobar que docker compose esta instalado

````
docker-compose --version
````
    
PASO 4: Crear topico SNS suscribirse al topico, indicar el cambio de la ARN.

PASO 5: Crear rol al EC2 > politica >sns Access

PASO 6: Ejecutar
````
    Sudo Docker compose up
````
    
PASO 7: Acceder al formulario, recibir un email (ver que se ha aceptado previamente el e-mail. Si no se encuentra mirar en correo no deseado / Spam)

> MICROSERVICES WITH DOCKER, PHP AND MYSQL
This is an example of a microservices implementation with Docker on AWS.
> 
> Microservices on AWS with Docker, PHP and MySQL represent a distributed application development architecture that leverages Amazon Web Services (AWS) cloud services along with technologies such as Docker, PHP and MySQL. Here I explain what each component entails:

Microservices: Instead of building a monolithic application, microservices break an application into small independent services, each focused on a specific task or business function. These services can be developed, deployed and scaled independently. This facilitates modularity, scalability and updating specific parts of the application without affecting the entire stack.

AWS (Amazon Web Services): A cloud services platform that offers a wide range of services to help businesses develop and run applications in a scalable and secure manner. AWS provides services such as cloud computing, storage, databases, analytics, machine learning, among others.

AWS (Amazon Web Services): AWS is a cloud services platform that offers a wide range of services to help companies develop and run applications in a scalable and secure way. AWS provides services such as cloud computing, storage, databases, analytics, machine learning, among others.

Docker: It is a container platform that allows packaging applications and their dependencies in virtualized and portable containers. Docker facilitates the creation, deployment and management of applications in development and production environments, by providing an isolated and consistent environment in any infrastructure.

PHP: It is a programming language widely used in web development. It is known for its simplicity and ease of use, as well as its large developer community and a large number of frameworks and libraries available for web development.

MySQL: It is an open source relational database management system widely used in web applications. It provides a fast, reliable and scalable database that integrates well with PHP and other web technologies.

When these components are combined in AWS, highly scalable and flexible microservice architectures can be built. For example, each microservice can be packaged in a Docker container and run on AWS using services such as Amazon Elastic Container Service (ECS) or Amazon Elastic Kubernetes Service (EKS). In addition, AWS provides database services such as Amazon RDS (Relational Database Service) that can be used to host MySQL databases in a scalable and managed manner. In summary, microservices on AWS with Docker, PHP and MySQL allow you to build modern applications that can easily scale to meet changing business demands.

STEP 1: Have AWS account

STEP 2: Install Docker Version 3.9

````
sudo yum update -y
sudo yum install -y docker
sudo usermood -a -G docker $(whoami)

````

STEP 3: Install Docker-compose

#download the binary to use docker-compose
````
    
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
````

 #give run permissions to the binary file
 ````
sudo chmod +x /usr/local/bin/docker-compose

````
#check that docker compose is installed

````
docker-compose --version
````
STEP 4: Create SNS topic subscribe to the topic, indicate the change of the ARN.

STEP 5: Create role to EC2 > policy >sns Access

STEP 6: Execute
 ````
    Sudo Docker compose up
````
STEP 7: Access the form, receive an email (check that the email has been previously accepted. If it is not found, check in junk mail / Spam).   
