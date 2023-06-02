# ¿Qué es Azure Cosmos DB y qué ventajas ofrece como servicio de base de datos?

````

Azure Cosmos DB es un servicio de base de datos multimodelo y distribuido globalmente, desarrollado y ofrecido por Microsoft como parte de su plataforma en la nube, Azure. Proporciona una solución escalable y altamente disponible para almacenar y consultar datos, ofreciendo varias ventajas significativas.

Distribución global: Azure Cosmos DB permite distribuir los datos en múltiples regiones geográficas de Azure, lo que garantiza una baja latencia y una alta disponibilidad para los usuarios en cualquier parte del mundo. Esto es especialmente útil para aplicaciones globales con usuarios distribuidos.

Escalabilidad elástica: Puedes escalar verticalmente (aumentar el rendimiento de una sola instancia) y escalar horizontalmente (agregar más instancias) según las necesidades de tu aplicación. Azure Cosmos DB puede manejar cargas de trabajo intensivas con una alta concurrencia y ofrecer un rendimiento consistente incluso en situaciones de alta demanda.

Modelos de datos flexibles: Azure Cosmos DB es una base de datos multimodelo, lo que significa que admite diferentes modelos de datos, como documentos, columnas, grafos y claves-valor. Esto te permite elegir el modelo de datos más adecuado para tu aplicación y aprovechar la flexibilidad para almacenar y consultar los datos de manera eficiente.

Consistencia y disponibilidad garantizadas: Azure Cosmos DB ofrece varios niveles de consistencia, desde una fuerte consistencia hasta una disponibilidad optimizada. Puedes elegir el nivel de consistencia adecuado para tus aplicaciones, lo que te permite equilibrar entre la coherencia y el rendimiento.

Multiplataforma y lenguajes de programación: Puedes acceder a Azure Cosmos DB desde diferentes plataformas, como Windows, Linux y macOS, y utilizar varios lenguajes de programación, como .NET, Java, Python, Node.js, entre otros. Esto facilita la integración con tus aplicaciones existentes y la elección de la tecnología adecuada para tu caso de uso.

Seguridad y cumplimiento normativo: Azure Cosmos DB ofrece características de seguridad avanzadas, como el cifrado de datos en reposo y en tránsito, el control de acceso basado en roles y la integración con Azure Active Directory. Además, cumple con varios estándares y certificaciones de cumplimiento normativo, lo que te permite cumplir con los requisitos regulatorios de tu industria.

Estas son solo algunas de las ventajas que ofrece Azure Cosmos DB como servicio de base de datos en la nube. Su flexibilidad, escalabilidad y disponibilidad global lo convierten en una opción atractiva para desarrolladores y empresas que buscan una solución de almacenamiento y consulta de datos altamente escalable y confiable.

````

# ¿Cuáles son los modelos de datos compatibles con Azure Cosmos DB?

````

Azure Cosmos DB es una base de datos distribuida globalmente y multimodelo. Esto significa que admite varios modelos de datos diferentes. A continuación se presentan los modelos de datos compatibles con Azure Cosmos DB:

Documentos: Azure Cosmos DB es conocido principalmente por su soporte nativo para el modelo de documentos. Los datos se almacenan en documentos JSON (JavaScript Object Notation) y se organizan en colecciones. Esto permite una gran flexibilidad en la estructura de los datos, ya que cada documento puede tener su propia estructura.

Gráficos: Azure Cosmos DB también admite el modelo de grafos, que es ideal para almacenar y consultar relaciones complejas entre entidades. El modelo de grafos utiliza nodos para representar entidades y bordes para representar relaciones entre ellas. Esto permite consultas eficientes para descubrir patrones y relaciones en los datos.

Clave-valor: Azure Cosmos DB admite el modelo de clave-valor, que es simple pero muy eficiente en términos de rendimiento. En este modelo, los datos se almacenan como pares clave-valor, donde cada valor se identifica mediante una clave única. Es útil para aplicaciones que requieren una alta velocidad de lectura y escritura.

Columnas amplias: Azure Cosmos DB ofrece soporte para el modelo de columnas amplias, también conocido como almacenamiento de columnas. Este modelo es especialmente útil para casos de uso analíticos en los que se requiere el procesamiento de grandes volúmenes de datos. Los datos se almacenan en columnas en lugar de filas, lo que permite consultas eficientes y rápidas en conjuntos de datos grandes.

Tuplas: Azure Cosmos DB también proporciona soporte para el modelo de tuplas. Las tuplas son una colección ordenada de elementos que pueden tener diferentes tipos de datos. Este modelo es útil para aplicaciones que requieren un almacenamiento flexible y estructuras de datos complejas.

Es importante tener en cuenta que Azure Cosmos DB es una base de datos NoSQL y está diseñada para ser escalable y tolerante a errores. Además, puede utilizar diferentes API para interactuar con estos modelos de datos, como SQL, MongoDB, Gremlin, Cassandra y Azure Table Storage API.
````

# ¿Cómo se accede y se realiza consultas a una base de datos de Cosmos DB en Azure?

````

Para acceder y realizar consultas a una base de datos de Cosmos DB en Azure, puedes seguir estos pasos:

Crear una instancia de Cosmos DB: Ve al portal de Azure (https://portal.azure.com) y crea una instancia de Cosmos DB. Selecciona el modelo de API adecuado según tus necesidades, como SQL, MongoDB, Cassandra, etc.

Configurar la base de datos: Después de crear la instancia de Cosmos DB, configura la base de datos y la colección dentro de ella. Define la configuración de particionamiento, las opciones de rendimiento y cualquier otra configuración necesaria.

Obtener las credenciales de conexión: Una vez creada la base de datos de Cosmos DB, obtén las credenciales de conexión necesarias para acceder a ella. Esto incluye la cadena de conexión y las claves de acceso, que se utilizarán para autenticarse y autorizarse en la base de datos.

Elegir un lenguaje de programación: Decide en qué lenguaje de programación deseas interactuar con Cosmos DB. Puedes elegir entre varios lenguajes, como C#, Java, Python, Node.js, etc. Asegúrate de que el SDK correspondiente esté instalado en tu entorno de desarrollo.

Instalar y configurar el SDK: Si estás utilizando un lenguaje de programación compatible, instala el SDK de Azure Cosmos DB correspondiente. Esto te permitirá interactuar con la base de datos utilizando el lenguaje elegido. Consulta la documentación oficial de Azure para obtener instrucciones detalladas sobre cómo instalar y configurar el SDK en tu entorno de desarrollo.

Conectarse a la base de datos: Utiliza la cadena de conexión proporcionada para establecer una conexión desde tu aplicación o código al servicio de Cosmos DB en Azure. Dependiendo del lenguaje de programación y el SDK que estés utilizando, habrá métodos y funciones específicas para establecer la conexión.

Realizar consultas: Una vez que te hayas conectado con éxito a la base de datos, puedes comenzar a realizar consultas. Las consultas se realizarán utilizando el lenguaje de consulta correspondiente según el modelo de API que hayas elegido. Por ejemplo, si estás utilizando el modelo de API de SQL, puedes usar consultas SQL para recuperar y manipular los datos.

Esos son los pasos generales para acceder y realizar consultas a una base de datos de Cosmos DB en Azure. Recuerda consultar la documentación oficial de Azure Cosmos DB y la documentación específica del SDK para obtener más detalles y ejemplos de código según tu lenguaje de programación preferido.
````

# Preguntas de la Batería

# Question 27 Pag 52

pdf correcto

[Referencia](https://learn.microsoft.com/en-us/azure/cosmos-db/consistency-levels)

1. Para asegurarnos tener los datos más recientes necesitaremos strong (Strong consistency offers a linearizability guarantee. Linearizability refers to serving requests concurrently. The reads are guaranteed to return the most recent committed version of an item. A client never sees an uncommitted or partial write. Users are always guaranteed to read the latest committed write.)
2. Con Bounded Staleness tenemos casi tanta seguridad como strong, tan solo podriamos tener alguna version anterior de los datos, no demasiado tardía
3. Well after the patient has been discharged there will be no more additions
   so consistency is not a huge concern, by this point it should be consistant across all the environments
   and eventual consistency is the fastest to access
