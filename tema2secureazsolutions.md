## Tema 2: Implement secure Azure solutions
### Preguntas:
- ¿Qué es Azure Key Vault y cómo se utiliza para proteger secretos y claves criptográficas?
    
      Azure Key Vault es un servicio de administración de secretos y claves criptográficas en Azure. Proporciona un lugar seguro para almacenar y gestionar secretos, como contraseñas, claves de API y certificados, junto con claves criptográficas utilizadas para proteger datos sensibles. Con Azure Key Vault, puedes almacenar estos secretos de manera segura y acceder a ellos de forma programática mediante API o integrarlos directamente en tus aplicaciones. Esto ayuda a proteger tus secretos de accesos no autorizados y garantiza que solo las aplicaciones y servicios autorizados puedan acceder a ellos. Azure Key Vault también ofrece características como el control de acceso granular y la generación segura de claves criptográficas, lo que proporciona una capa adicional de seguridad para proteger tus datos confidenciales.

- ¿Cuál es el papel de las Identidades Administradas (Managed Identities) en la seguridad de Azure
    
      Las Identidades Administradas (Managed Identities) desempeñan un papel fundamental en la seguridad de Azure al proporcionar una forma segura y conveniente de autenticar y autorizar recursos en la nube. Con las Identidades Administradas, no es necesario gestionar ni almacenar credenciales o claves de acceso. En su lugar, Azure se encarga de generar y gestionar automáticamente las Identidades Administradas para los recursos que las necesitan. Esto significa que los recursos pueden autenticarse y acceder a otros servicios de Azure de manera segura sin necesidad de exponer credenciales sensibles. Las Identidades Administradas se integran con los servicios de Azure para proporcionar una autenticación sin problemas y reducir los riesgos asociados con el manejo de credenciales. En resumen, las Identidades Administradas son una herramienta poderosa para fortalecer la seguridad en Azure al simplificar la autenticación y minimizar las vulnerabilidades relacionadas con el manejo de credenciales.
  
- ¿Cómo se configuran y se utilizan Azure Key Vault y las Identidades Administradas?

      Para configurar y utilizar Azure Key Vault con Identidades Administradas, primero debes crear un Azure Key Vault en el portal de Azure. Luego, debes habilitar la Identidad Administrada para el recurso que necesitará acceder al Key Vault, como una máquina virtual o una función de Azure. Después de habilitar la Identidad Administrada, puedes otorgar permisos de acceso al Key Vault para que la Identidad Administrada pueda acceder a los secretos y claves almacenados de manera segura. A continuación, en el código de tu aplicación, puedes utilizar la Identidad Administrada para autenticarte con Azure Key Vault y acceder a los secretos y claves necesarios sin necesidad de almacenar credenciales en el código fuente. Esto proporciona una capa adicional de seguridad al evitar la exposición de credenciales sensibles y permite una gestión centralizada de secretos en Azure Key Vault.
  

### Identificar y explicar (comprobar si es posible) de la batería de Preguntas 3 preguntas por cada integrante relacionadas con Azure Key Vault y Managed Identities
- QUESTION 14, p.: 36

      You are developing a serverless Java application on Azure. You create a new Azure Key Vault to work with secrets from a new Azure Functions application.
      
      The application must meet the following requirements:
       - Reference the Azure Key Vault without requiring any changes to the Java code.
       - Dynamically add and remove instances of the Azure Functions host based on the number of incoming application events.
       - Ensure that instances are perpetually warm to avoid any cold starts.
       - Connect to a VNet.
       - Authentication to the Azure Key Vault instance must be removed if the Azure Function application is deleted.
      
      You need to grant the Azure Functions application access to the Azure Key Vault. 

      Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
    ![image](/img/q14_1.png)
      Correct Answer:

    ![image](/img/q14_2.png)

    Explicación:
     
      Paso 1: Crea la aplicación de Azure Functions con un tipo de plan de consumo. Utiliza el plan de consumo para el uso de servidor sin servidor (serverless).

      Paso 2: Crea una identidad administrada asignada por el sistema para la aplicación. Crea una identidad administrada asignada por el sistema para tu aplicación.
      Actualmente, las referencias a Key Vault solo admiten identidades administradas asignadas por el sistema. Las identidades asignadas por el usuario no se pueden utilizar.
      
      Paso 3: Crea una política de acceso en Key Vault para la identidad de la aplicación que creaste anteriormente. Habilita el permiso "Obtener" secretos en esta política. No configures la "aplicación autorizada" o los ajustes de applicationId, ya que esto no es compatible con una identidad administrada.

- QUESTION 33, p 59

      HOTSPOT
      You are developing an application that needs access to an Azure virtual machine (VM).

      The access lifecycle for the application must be associated with the VM service instance.

      You need to enable managed identity for the VM.

      How should you complete the PowerShell segment? To answer, select the appropriate options in the answer area.

      NOTE: Each correct selection is worth one point.

    ![image](/img/Q33.png)

    Explicación:
     
      En el cuadro 1, se muestra cómo habilitar una identidad administrada asignada por el sistema en una máquina virtual de Azure existente. Esto se logra utilizando el interruptor -IdentityType en el cmdlet Update-AzVM. Al establecer el valor en "SystemAssigned", se habilita la identidad administrada asignada por el sistema en la máquina virtual.
      
      En el cuadro 2, se presenta un ejemplo de código en PowerShell para realizar esta acción. Se obtiene la referencia a la máquina virtual con el cmdlet Get-AzVM y luego se utiliza el cmdlet Update-AzVM para actualizar la máquina virtual con la opción -IdentityType establecida en "SystemAssigned". Esto activará la identidad administrada asignada por el sistema en la máquina virtual especificada en el grupo de recursos indicado.

- QUESTION 24, p 162

      You are developing a medical records document management website. The website is used to store scanned copies of patient intake forms.
      
      If the stored intake forms are downloaded from storage by a third party, the contents of the forms must not be compromised.
      
      You need to store the intake forms according to the requirements. Solution: Store the intake forms as Azure Key Vault secrets.
      
      Does the solution meet the goal?
      A. Yes 
      B. No

      Correct Answer: B
    Explicación:

      Azure Key Vault es un servicio que se utiliza para almacenar y administrar secretos, claves y certificados. Sin embargo, en este escenario, no es la solución adecuada para almacenar los formularios de admisión de pacientes.

      En cambio, sería más adecuado utilizar Azure Blob Storage, para almacenar los formularios de admisión. Se pueden aplicar medidas adicionales de seguridad, como la encriptación de datos en reposo y el control de acceso, para garantizar que el contenido de los formularios no se comprometa si son descargados por terceros.

