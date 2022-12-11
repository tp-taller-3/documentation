# Convenciones generales

* Las carpetas y archivos que refieren a entidades (en singular) como `Database`, `Environment`, `Admin`, `Logger` van en mayúscula.

* Las carpetas y archivos que actúan como contenedores (en general, en plural) 
como `graphql`, `config`, `models`, `migrations`, `defaultTranslations`, 
`queries`, `fieldTypes` van en minúscula. También los "sustantivos comunes", 
como `compontent` y `container` dentro de `NavBar`.

* No utilizar default export. Es preferible nombrar los exports (ejemplo: `export Database` en `Database.ts`)

* La estructura de carpetas de `/test` tiene que imitar la estructura de `/src`.

* Archivos y carpetas:
    * Para componentes react y types de graphql usar CamelCase.

* Las carpetas de los modelos en singular (`Semester`). Dentro de la carpeta se pueden guardar los 
archivos `Model.ts`, `Repository.ts`, `Interface.ts`, etc.

* Los modelos se llaman sin ningún sufijo ni prefijo.

* Los tipos de `GraphQL` se guardan en una carpeta `Types` dentro de la carpeta de la entidad correspondiente
    * Esta tiene un index con un array y todos los types

* Los tipos de `GraphQL` se nombran como: **GraphQL&lt;TypeName&gt;**. Ejemplo: `GraphQLSemester`

* El ancho mínimo de viewport que soportamos es de 290px inclusive

* Todas las Queries y Mutations de Graphql deben ser guardadas en constantes en mayúsculas al momento de ser usadas.

## Convenciones del Front End

* La aplicación está dividida en páginas, cada una con su ruta. Las rutas 
se declaran en `RoutesBuilder` y cada una corresponde a un componente 
"page", en la carpeta `src/pages`.

* Los componentes que son comunes a varias páginas deben ser guardados en la 
carpeta `src/components`.

* Los componentes que se usan solo en una page, deben ser escritos en la 
carpeta de la page.

* Todos los componentes se escriben dentro de una carpeta con el nombre del 
componente con la primer letra en mayúscula.

* En un principio, si una interfaz se usa solo en un archivo, la interfaz se 
declara ahí mismo. Si se necesita en dos archivos distintos, se la declara en 
un archivo `interfaces.ts`, en la carpeta donde se lo considere más apropiado.
