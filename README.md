# AddressBook

El programa AddressBook es una aplicación en Java que gestiona una agenda de contactos, permitiendo almacenar, visualizar y eliminar información. Utiliza un HashMap<String, String> para almacenar los contactos, con el número telefónico como clave y el nombre como valor. Además, los datos se guardan en un archivo CSV para persistencia.

Funcionamiento detallado
1. Inicio y carga de datos
Al ejecutar la aplicación, el constructor de AddressBook llama al método load(), que lee el archivo contacts.csv, carga los contactos en el HashMap, y los prepara para ser utilizados en la agenda.

2. Menú interactivo
El programa presenta al usuario un menú con tres opciones principales:

Listar contactos (list()): Itera sobre el HashMap y muestra los contactos en el formato {Número} : {Nombre}.

Crear contacto (create()): Solicita al usuario el número y el nombre, los guarda en el HashMap, y luego persiste los cambios en contacts.csv.

Eliminar contacto (delete()): Solicita un número telefónico, verifica si existe en el HashMap y lo elimina si es encontrado, actualizando el archivo CSV.

3. Almacenamiento de contactos en CSV
Cada vez que se crea o elimina un contacto, el método save() sobrescribe contacts.csv con la información actualizada. El formato del archivo es:

5551234567,Juan Pérez  
5569876543,Maria Gómez  
Esto garantiza que los datos persistan entre ejecuciones.

4. Ejecución y cierre
El menú sigue ejecutándose en un ciclo do-while, permitiendo al usuario gestionar contactos hasta que seleccione la opción de salir.
