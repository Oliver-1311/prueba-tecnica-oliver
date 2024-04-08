# Proyecto de Automatización de Recolección de Datos de Sensores

Este proyecto consiste en el desarrollo de una aplicación web compuesta por un frontend y un backend para automatizar el proceso de recolección de datos de sensores, así como para calcular y mostrar promedios de los valores obtenidos.

## Contenido

1. [Frontend](#frontend)
2. [Backend](#backend)
3. [Instrucciones de Ejecución](#instrucciones-de-ejecución)
4. [Consideraciones](#consideraciones)
5. [Autor](#autor)

## Frontend

El frontend de la aplicación web está desarrollado en React.js y consta de dos páginas:

- **/carga:** Vista donde se sube el archivo CSV con la información de los sensores.
- **/resumen:** Vista donde se muestra una tabla con el resumen de los valores promedio de los sensores.

### Dockerización

El frontend está contenerizado mediante Docker para facilitar su despliegue y ejecución en diferentes entornos.

## Backend

El backend de la aplicación es un API desarrollado en Flask (Python) para el procesamiento de la carga de datos de los sensores y la generación de los promedios.

### Endpoints

- **api/v1/load:** Acepta un array de objetos de la carga y realiza el procesamiento para generar promedios por sensor, almacenando la información en las tablas `measurement_detail` (registro de la medición) y `summary` (registro del promedio del sensor).
- **api/v1/list:** Obtiene los datos de los promedios de los sensores de la tabla `summary`.

### Base de Datos

Se utiliza una base de datos local como MySQL o PostgreSQL para almacenar los registros de las mediciones y los promedios.

### Dockerización

El backend también está contenerizado mediante Docker para facilitar su despliegue y ejecución.

## Instrucciones de Ejecución

Para ejecutar la aplicación, sigue los siguientes pasos:

1. Clona este repositorio en tu máquina local.
2. Navega a la carpeta del proyecto.
3. Levanta los contenedores Docker para el frontend y el backend utilizando los archivos Docker-compose proporcionados.
4. Accede a la aplicación web desde tu navegador.

## Consideraciones

- Asegúrate de tener Docker instalado en tu sistema antes de ejecutar la aplicación.
- Los archivos CSV deben seguir el formato especificado para que el procesamiento sea correcto.
- Verifica que la base de datos esté configurada correctamente antes de ejecutar la aplicación.

## Autor

Este proyecto fue desarrollado por Oliver Macedo.
