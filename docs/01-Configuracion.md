# Configuración inicial

1. Abre una terminal o símbolo del sistema en tu equipo

2. Ejecuta el siguiente comando para clonar el repositorio del proyecto que vamos a implementar en Azure.

    `git clone https://github.com/Azure-Samples/nodejs-appsvc-cosmosdb-bottleneck.git`

3. Abre Visual Studio Code y desde el menú `Archivo`, elige `Abrir carpeta...`. Selecciona la carpeta `nodejs-appsvc-cosmosdb-bottleneck` que clonaste.

4. Confía en los autores en caso que te aparezca dicha solicitud.

5. En Visual Studio Code, en el menú `Terminal`, abre una `Nueva terminal` de tipo `PowerShell`.

6. Ejecuta el siguiente comando para iniciar sesión en Azure (NOTA: Este comando requiere que tengas instalada la CLI de Azure):

    `az login`

7. Ingresa tus credenciales o confirma la cuenta de Azure que deseas utilizar.

8. Elige la suscripción que deseas usar de la lista que aparece. En caso de que no te aparezca, puedes usar el siguiente comando:

    `az account set --subscription AzureSubscriptionID`

    - Reemplaza `AzureSubscriptionID` por el id de la suscripción de Azure a utilizar (puedes consultarlo desde el Portal de Azure).

9. Ejecuta el siguiente comando para implementar la aplicación en Azure:

    `.\deploymentscript.ps1`

10. El script te solicitará la siguiente información:

    - Suscripción de Azure a utilizar
    - Nombre único para la aplicación web y los recursos (agrega números para que sea único, utiliza letras minúsculas de preferencia).
    - Una región de Azure para la ubicación de los recursos. Se ha probado con la región `northeurope` de forma satisfactoria, y también se ha verificado que la región *eastus* provoca un error debido a la alta demanda.

11. Cuando el script finalice después de unos minutos, aparecerá la URL de la aplicación implementada. Haz clic en el enlace para navegar a la página web.

12. Verifica el funcionamiento de tres endpoints:

    - /
    - /get
    - /lasttimestamp

13. Observa que se actualiza el contador y la información de última visita en la página. Esta información se almacena en una base de datos de CosmosDB.

14. Navega al portal de Azure, localiza el grupo de recursos creado y la lista de recursos que fueron implementados gracias al script.

En el siguiente ejercicio, crearás un recurso de Azure Load Testing.

[Continúa en la siguiente página](./02-AzureLoadTesting.md)