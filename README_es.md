# Ejemplos del Contenido de los paquetes

[![goodtables.io](https://goodtables.io/badge/github/frictionlessdata/example-data-packages.svg)](https://goodtables.io/github/frictionlessdata/example-data-packages)


Este repositorio contiene ejemplos del contenido de los paquetes para ayudarte a aprender sobre el [Contenido Frictionless](https://frictionlessdata.io/). Un ejemplo de los contenido de los paquetes:

- ilustraciones sobre los paquetes actuales con contenido Frictionless [Especificaciones](https://frictionlessdata.io/specs/)
- ayuda al contenido Frictionless [Guías](https://frictionlessdata.io/guides/)
- demostraciones de contenido Frictionless [Formas](https://frictionlessdata.io/specs/patterns/) - formas para resolver problemas comunes que (aún) no están en las especificaciones

Las guías son una excelente forma de [empezar a aprender](https://frictionlessdata.io/guides/). Otra forma sería abriendo el directorio del contenidos de los paquetes, vea los `README.md`, luego vea el `datapackage.json` para entender el contenido.

*Advertencia: algunos paquetes de datos están desactualizados. (Vea el [Issue #4](https://github.com/frictionlessdata/example-data-packages/issues/4))*

## El contenido del paquete

El `datapackage.json` describirá el [contenido del paquete](https://frictionlessdata.io/specs/data-package/) como un todo, y uno o más [recurso del contenido](https://frictionlessdata.io/specs/data-resource/) (cada uno puede que tenga su [esquema](https://frictionlessdata.io/specs/data-resource/#resource-schemas) o su [visualizacion](https://frictionlessdata.io/specs/views/)).

Si todo el contenido es tabular (es decir [archivos CSV](https://frictionlessdata.io/guides/csv/)), entonces será describido como un [contenido de paquete tabular](https://frictionlessdata.io/specs/tabular-data-package/) con uno o más [recursos de contenido tabular](https://frictionlessdata.io/specs/tabular-data-package/) todos con su [tabla de esquemas](https://frictionlessdata.io/specs/table-schema/) and, if needed, a [CSV dialect](https://frictionlessdata.io/specs/csv-dialect/).

Existen otras especialidades en los [perfiles](https://frictionlessdata.io/specs/profiles/) que describen los diferentes tipos de contenido, tales como [contenido fiscal](https://frictionlessdata.io/specs/fiscal-data-package/).

Todo el contenido del paquete es almacenado en su propio directorio:

```
|- data-package-name-1
   |- README.md
   |- datapackage.json
   |- data
      |- data.csv
      |- ...
```

Este contiene:

- `README.md` que explique de donde proviene el contenido
- `datapackage.json` un archivo legible que explique la estructura y el significado del contenido
- uno o más archivos, que normalmente son agrupados en un directorio de `data` 

El contenido del paquete puede que tambien contenga [otros archivos o subdirectorios](https://frictionlessdata.io/specs/data-package/#illustrative-structure). Estos archivos pueden ser scripts utilizados para preparar el contenido del paquete o otros recursos relacionados.

## Aprobación

### Aprobación del Repositorio

Con cada ajuste al repositorio, el contenido del paquete será aprobado utilizando [goodtables.io](http://goodtables.io/). El resultado de la aprobación del conteido de los paquetes se especifica en [goodtables.yml](goodtables.yml) son indicados con una insignia: ![goodtables.io](https://goodtables.io/badge/github/frictionlessdata/example-data-packages.svg)

*Idealmente se otorgará una insignia por cada contenido de paquete y será visible en su archivo `README.md`  pero esto aún no es posible. (Vealo en goodtables.io [issue #285](https://github.com/frictionlessdata/goodtables.io/issues/285))*

La aprobación es controlada por el archivo [goodtables.yaml](https://github.com/frictionlessdata/example-data-packages/blob/master/goodtables.yml). Este debe ser configurado para que pruebe cada contenido de los paquetes en el repositorio. Esto podrá ser cambiado si trabaja localmente para [validar el contenido de un paquete en especifico](https://github.com/frictionlessdata/goodtables.io/blob/master/docs/goodtables_yml.md).

### Aprobación Local

Queremos implementar la [aprobación local](https://github.com/frictionlessdata/example-data-packages/issues/6) para que los paquetes puedan ser aprobados antes de ser contribuidos en este repositorio.

## Comprimir el contenido de los paquetes

Con cada ajuste al repositorio, el directorio con el contenido del paquete será convertido en un archivo .zip para que pueda ser usado con un [software que ejecute el contenido Frictionless](https://frictionlessdata.io/software/) tal como el [Curador de Contenido](http://data-curator.io) app or the [DataPackage.js](https://github.com/frictionlessdata/datapackage-js) library. The zip files are stored in the `zip` directory.

Mientras que [no se haya finalizado la compresión del contenido de los paquetes](https://github.com/frictionlessdata/specs/issues/132) un numero de [Software de contenido Frictionless](https://frictionlessdata.io/software/) implementaciones compatibles al archivo _zip_ comprimido.

*Para esto: es necesario script*

## Formateo de JSON

Con cada ajuste, el archivo `datapackage.json` será [formateado para ser más fácil de leer](https://frictionlessdata.io/guides/publish-faq/#alignment). Aunque este formateo no sea necesario en programas de computador, Te hace más fácil para ver el contenido del archivo.

*Para esto: es necesario script (o linting)*

## Recursos

Los recursos del directorio contienen la planilla `README.md` y fragmentos de `datapackage.json`.

### Planilla `README.md` 

En este repositorio, cada contenido de paquete debe tener un `README.md`. El `README.md` debe tener [buena legibilidad](https://frictionlessdata.io/guides/publish-faq/#readme).

### Fragmentos de `datapackage.json` 

Los fragmentos de JSON proveen un archivo `datapackage.json` para ayudarte a aprender sobre una propiedad especifica o a copiar y pegar en tu propio contenido del paquete P.ej. `licenses.json` puede incluir un JSON para cada [recomendación de Open Definition conforme a su licencia](http://opendefinition.org/licenses/#conformant-licenses).

## Estructura del Repositorio

```
|
|- data-package-name-1
|  |- README.md
|   |- datapackage.json
|   |- data
|     |- data.csv
|     |- data.geojson
|     |- ...
|     
|- data-package-name-2
|  |- etc.
|
|- resources
|  |- README-template.md
|  |- licenses.json
|  |- contributors.json
|  |- dialect.json
|  |- ...
|
|- zip
|  |- data-package-name-1.zip
|  |- data-package-name-2.zip
|
|
|- goodtables.yaml
|- README.md   

```

## Contribución

Apreciamos todo tipo de colaboración:
- documentación
- Contenidos
- [issues](https://github.com/frictionlessdata/example-data-packages/issues) y [requests](https://github.com/frictionlessdata/example-data-packages/issues)
- códigos

Agradecemos nuestros generosos [colaboradores](https://github.com/frictionlessdata/example-data-packages/graphs/contributors) de este proyecto.

Para unirse, Porfavor leer el [`CONTRIBUTING.md`](.github/CONTRIBUTING.md) para los detalles sobre nuestro código de conducta y como solicitar un pull request. Cada contenido del paquete contribuido deberá tener una licencia abierta.

## Licencias

El contenido de paquetes en este proyecto será licenciado como se especifique en cada archivo `datapackage.json`. Si no se especifica una licencia, se proveerá bajo un [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) dominio público.

El código de este proyecto, a menos que se indique lo contrario, tendrá la licencia que se describe en [`LICENSE.md`](LICENSE.md).