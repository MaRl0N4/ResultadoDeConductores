# Formula 1 Driver Results TableView

Esta aplicación JavaFX permite visualizar los resultados de los conductores de Formula 1 en un `TableView`, basado en los datos obtenidos de una base de datos PostgreSQL. Los usuarios pueden seleccionar un año específico desde un `ComboBox` y los resultados correspondientes se mostrarán en la tabla.

## Características

- Selección de año mediante un `ComboBox`.
- Visualización de resultados en un `TableView` con las columnas: `DriverName`, `Wins`, `TotalPoints`, `Rank`.

## Requisitos

- Java 11 o superior.
- PostgreSQL.
- Librerías de JavaFX.

## Configuración de la Base de Datos

1. Instala PostgreSQL y crea una base de datos llamada `Formula1N`.
2. Asegúrate de tener las siguientes tablas y datos en tu base de datos:
    - `drivers`
    - `races`
    - `results`
    - `seasons`

## Instalación

1. Clona el repositorio:
    ```sh
    git clone https://github.com/tu_usuario/driver-results-viewer.git
    cd driver-results-viewer
    ```

2. Configura las credenciales de la base de datos en la clase `DriverResultRepository`:
    ```java
    String jdbcURL = "jdbc:postgresql://localhost:5432/Formula1N";
    String username = "postgres";
    String password = "tu_password";
    ```

3. Ejecuta la aplicación:
    ```sh
    ./gradlew run
    ```

## Estructura del Proyecto

- `Main.java`: Clase principal que inicia la aplicación.
- `DriverResultsWindow.java`: Clase que crea la ventana con el `TableView` para mostrar los resultados de los conductores.
- `Repositories/DriverResultRepository.java`: Clase que maneja la conexión a la base de datos y las consultas de resultados de los conductores.
- `Repositories/SeasonRepository.java`: Clase que maneja la conexión a la base de datos y las consultas de temporadas.
- `Models/DriverResult.java`: Clase modelo para los resultados de los conductores.
- `Models/Season.java`: Clase modelo para las temporadas.

## Uso

1. Ejecuta la aplicación.
2. Selecciona un año desde el `ComboBox`.
3. Los resultados de los conductores se mostrarán en el `TableView`.

## Contribución

Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y envía un pull request con tus cambios.

## Licencia

Este proyecto está licenciado bajo los términos de la licencia MIT.

## Capturas de la ejecución de la App:
![EJCUCIÓN APP](https://github.com/MaRl0N4/ResultadoDeConductores/blob/41b77cecb213a2b2db9e0c8baf941491f9b09c15/Captura%20de%20pantalla%20(480).png)
![EJCUCIÓN APP](https://github.com/MaRl0N4/ResultadoDeConductores/blob/a4285089987928b04cb6b8e044cc3faef28b0f4a/Captura%20de%20pantalla%20(481).png).

