# # Tarea (a+b) · Cloud: niveles y funciones (DAW 1º)

## 🅰️ Tarea A — Niveles de cloud (IaaS/PaaS/SaaS)
Crea una tabla con 10 servicios reales. Incluye enlace oficial y justifica responsabilidades.

| **Servicio**           | **Proveedor** | **Nivel**      | **Enlace oficial**                                                                                                           | **¿Qué gestiona el proveedor?**                    | **¿Qué gestiona el equipo/usuario?**                                      |
| ---------------------- | ------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------- |
| Amazon EC2             | AWS           | IaaS           | [https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/)                                                                   | Hardware, red, virtualización| SO, middleware, apps, datos ([Wikipedia][1])                              |
| Azure Virtual Machines | Microsoft     | IaaS           | [https://azure.microsoft.com/en-us/services/virtual-machines/](https://azure.microsoft.com/en-us/services/virtual-machines/) | Infraestructura (servidores, red, almacenamiento)  | Sistema operativo, apps, datos ([CloudZero][2])                           |
| Google Compute Engine  | Google Cloud  | IaaS           | [https://cloud.google.com/compute](https://cloud.google.com/compute)                                                         | Infraestructura física y virtualización          | OS, apps y datos ([CloudZero][2])                                         |
| AWS S3                 | AWS           | IaaS (Storage) | [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)                                                                     | Gestión de infraestructura de almacenamiento       | Organización de datos, permisos de acceso ([CloudZero][2])                |
| Google App Engine      | Google Cloud  | PaaS           | [https://cloud.google.com/appengine/](https://cloud.google.com/appengine/)                                                   | Plataforma runtime, balanceo, escalado automático  | Código de app, configuración lógica ([Wikipedia][3])                      |
| Azure SQL Database     | Microsoft     | PaaS           | [https://azure.microsoft.com/en-us/products/azure-sql/](https://azure.microsoft.com/en-us/products/azure-sql/)               | Base de datos gestionada, parches, backups         | Esquema, consultas, datos de negocio ([Wikipedia][4])                     |
| AWS Elastic Beanstalk  | AWS           | PaaS           | [https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)                                         | Plataforma de despliegue, escalado y runtime       | Código de la app, configuración de despliegue ([ICS][5])                  |
| Google Workspace       | Google        | SaaS           | [https://workspace.google.com/](https://workspace.google.com/)                                                               | App, mantenimiento, seguridad y datos básicos      | Uso de apps, gestion deusuarios, datos de organización ([Stackscale][6]) |
| Salesforce CRM         | Salesforce    | SaaS           | [https://www.salesforce.com/](https://www.salesforce.com/)                                                                   | App CRM completa, infraestructura, actualizaciones | Configuración de workflows, datos CRM ([Stackscale][6])                   |
| Microsoft 365          | Microsoft     | SaaS           | [https://www.microsoft.com/microsoft-365](https://www.microsoft.com/microsoft-365)                                           | Aplicaciones completas, actualizaciones, seguridad | Gestión de usuarios, datos, políticas internas ([Stackscale][6])          |

[1]: https://en.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud?utm_source=chatgpt.com "Amazon Elastic Compute Cloud"
[2]: https://www.cloudzero.com/blog/cloud-service-providers/?utm_source=chatgpt.com "21+ Top Cloud Service Providers Globally In 2025"
[3]: https://en.wikipedia.org/wiki/Google_App_Engine?utm_source=chatgpt.com "Google App Engine"
[4]: https://en.wikipedia.org/wiki/Microsoft_Azure_SQL_Database?utm_source=chatgpt.com "Microsoft Azure SQL Database"
[5]: https://ics.com.es/informatica/20-ejemplos-de-paas-plataforma-como-servicio/?utm_source=chatgpt.com "20 Ejemplos de PaaS (Plataforma como Servicio) - ICS"
[6]: https://www.stackscale.com/es/blog/modelos-de-servicio-cloud/?utm_source=chatgpt.com "Modelos de servicio cloud: IaaS, PaaS y SaaS"


## 🅱️ Tarea B — Funciones principales de cloud (arquitectura)
Incluye un diagrama (ASCII/Mermaid/imagen) y una explicación breve.

### Diagrama
```
  |Usuario|
      |
      v
  |Aplicación (web/app)|
      |
      v
  |Servidor en la nube|
      |
  +------------------+
  |                  |
|Base de datos|   |Almacenamiento|
      |
   |Copia de
   seuridad|
```
### Explicación (8–12 líneas)
(Describe el flujo front → API → BBDD/storage y dónde entra la cloud)

Cuando un usuario usa una aplicación, primero interactúa con el front (la parte que ve en su navegador o móvil).
El front envía las solicitudes a la API, que es como un intermediario que sabe cómo hablar con la base de datos y el almacenamiento.
La API procesa la información y pide datos a la base de datos (donde se guardan cosas como usuarios, contraseñas o pedidos) o al almacenamiento (para fotos, archivos o vídeos).
La cloud entra aquí porque todo esto no está en tu ordenador, sino en servidores por internet que la empresa alquila.
Esos servidores se encargan de que la app funcione 24/7, que los datos estén seguros y que se pueda acceder desde cualquier lugar.
Si hay muchos usuarios a la vez, la cloud permite que se añadan más servidores para que la app no se caiga.
Además, hace copias de seguridad automáticamente por si algo falla.
Así, tú como programador solo te preocupas de la app y los datos, y la cloud gestiona la infraestructura y la disponibilidad.

### Mapeo de funciones cloud a componentes (mínimo 3)

Procesamiento → Servidores en la nube
Los servidores hacen los cálculos y ejecutan la lógica de la aplicación cuando los usuarios hacen solicitudes.

Ejecución → Aplicación / API
La app o la API se encarga de recibir lo que pide el usuario y enviar las respuestas adecuadas.

Almacenamiento → Base de datos y almacenamiento en la cloud
Aquí se guardan los datos de los usuarios, archivos, imágenes, vídeos y copias de seguridad.

Intercambio → Red / Internet (opcional)
Permite que el front del usuario y la API se comuniquen a través de la nube de manera segura y rápida.

## 📚 Fuentes (enlaces oficiales)
(Enlaces oficiales usados en la tabla A y en la B)

### Tabla A — Servicios Cloud
- **Amazon EC2 (IaaS)**: [https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/)  
- **Azure Virtual Machines (IaaS)**: [https://azure.microsoft.com/en-us/services/virtual-machines/](https://azure.microsoft.com/en-us/services/virtual-machines/)  
- **Google Compute Engine (IaaS)**: [https://cloud.google.com/compute](https://cloud.google.com/compute)  
- **AWS S3 (Almacenamiento IaaS)**: [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)  
- **Google App Engine (PaaS)**: [https://cloud.google.com/appengine](https://cloud.google.com/appengine)  
- **Azure SQL Database (PaaS)**: [https://azure.microsoft.com/en-us/products/azure-sql/](https://azure.microsoft.com/en-us/products/azure-sql/)  
- **AWS Elastic Beanstalk (PaaS)**: [https://aws.amazon.com/elasticbeanstalk/](https://aws.amazon.com/elasticbeanstalk/)  
- **Google Workspace (SaaS)**: [https://workspace.google.com/](https://workspace.google.com/)  
- **Salesforce CRM (SaaS)**: [https://www.salesforce.com/](https://www.salesforce.com/)  
- **Microsoft 365 (SaaS)**: [https://www.microsoft.com/microsoft-365](https://www.microsoft.com/microsoft-365)  

### Tarea B — Arquitectura / funciones cloud
- **Qué es Cloud Computing (Microsoft)**: [https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/)  
- **Google Cloud - Introducción a App Engine**: [https://cloud.google.com/appengine/docs](https://cloud.google.com/appengine/docs)  
- **Conceptos básicos de IaaS, PaaS y SaaS**: [https://stackscale.com/es/blog/modelos-de-servicio-cloud/](https://stackscale.com/es/blog/modelos-de-servicio-cloud/)
