# ¿Cuál es la diferencia entre Azure Message Queue, Azure Service Bus y Azure Queue Storage en términos de funcionalidad y casos de uso?

````

Azure Message Queue, Azure Service Bus y Azure Queue Storage son servicios de mensajería y encolamiento ofrecidos por Azure, pero tienen diferencias en términos de funcionalidad y casos de uso. La elección entre Azure Message Queue, Azure Service Bus y Azure Queue Storage depende de los requisitos específicos de tu aplicación. Si necesitas una cola de mensajes simple sin funcionalidades avanzadas, Azure Message Queue puede ser suficiente. Para casos de uso más complejos y avanzados, como la integración de sistemas, la mensajería empresarial o el procesamiento de eventos, Azure Service Bus es la opción más adecuada. Si buscas una solución económica y escalable para almacenar y encolar grandes cantidades de mensajes sin características avanzadas, Azure Queue Storage es una buena opción.

````

# ¿Cómo se utiliza Azure Message Queue para el envío y recepción de mensajes entre componentes de una aplicación distribuida?

````

1. Crear una instancia de Azure Message Queue

2. Enviar mensajes a la cola

3. Configurar el receptor de mensajes

4. Recibir mensajes de la cola

5. Confirmar y eliminar mensajes

6. Escalar y gestionar la cola

````

# ¿Cuál es el propósito y la ventaja de utilizar Azure Service Bus en comparación con otros servicios de mensajería?

````

El propósito principal de Azure Service Bus es proporcionar un servicio de mensajería fiable y escalable en entornos distribuidos. Permite la comunicación entre componentes de aplicaciones y sistemas a través del intercambio de mensajes. En comparación con otros servicios de mensajería, Azure Service Bus se destaca por su confiabilidad, escalabilidad y flexibilidad en el manejo de mensajes. Es especialmente adecuado para aplicaciones empresariales que requieren una mensajería confiable y asincrónica, como sistemas de pedidos, procesamiento de eventos en tiempo real y comunicación entre componentes distribuidos.

````

# Preguntas de la Batería

# QUESTION 16 - Pagina 209

**A. Assign the value of the hazard message SessionID property to the ReplyToSessionId property.**
B. Assign the value of the hazard message MessageId property to the DevileryCount property.
C. Assign the value of the hazard message SessionID property to the SequenceNumber property.
**D. Assign the value of the hazard message MessageId property to the CorrelationId property.**
E. Assign the value of the hazard message SequenceNumber property to the DeliveryCount property.
F. Assign the value of the hazard message MessageId property to the SequenceNumber property.

# QUESTION 2 - Pagina 219

A. Azure Event Grid topic
B. Azure Service Bus topic
**C. Azure Service Bus queue**
D. Azure Storage queue
E. Azure Logic App custom connector

# QUESTION 7 - Pagina 232

**A. Azure Storage Queue**
B. Azure Event Hub
C. Azure Service Bus
D. Azure Event Grid