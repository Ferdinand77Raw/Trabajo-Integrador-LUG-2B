TRABAJO PRACTICO INTEGRADOR - LUG 2B
------------------------------------------------------------

Este proyecto fue desarrollado en C# (.NET Framework) utilizando Windows Forms.
Se trabaja bajo una arquitectura en capas, separando la interfaz gráfica, la lógica de negocio y el acceso a datos.

------------------------------------------------------------
ESTRUCTURA DEL PROYECTO
------------------------------------------------------------
.vs/                     -> Archivos temporales de Visual Studio (no versionar)
bin/                     -> Archivos compilados (.exe, .dll)
obj/                     -> Archivos intermedios de compilación
BLL/                     -> Capa de lógica de negocio (Business Logic Layer)
DAL/                     -> Capa de acceso a datos (Data Access Layer)
UI/                      -> Capa de interfaz gráfica (Windows Forms)
Properties/              -> Configuraciones del proyecto (.NET)
Class1.cs                -> Clases auxiliares o genéricas
Entity.csproj            -> Archivo de proyecto principal
LICENSE                  -> Licencia del proyecto
TrabajoPracticoIntegrador-LUG-2B.sln -> Solución principal

IMPORTANTE:
Las carpetas .vs, bin, obj y archivos temporales de usuario no deben subirse al repositorio (.gitignore).

------------------------------------------------------------
REQUISITOS PREVIOS
------------------------------------------------------------
- Visual Studio 2019 o 2022 (con carga de trabajo "Desarrollo de escritorio con .NET")
- .NET Framework 4.x (versión según .csproj)
- Git instalado
- Acceso al repositorio de GitHub del grupo

------------------------------------------------------------
COMO CLONAR Y EJECUTAR EL PROYECTO
------------------------------------------------------------
1. Abrir una terminal o Git Bash.
2. Clonar el repositorio:
   git clone https://github.com/<ORGANIZACION>/<NOMBRE-REPO>.git
   cd <NOMBRE-REPO>
3. Abrir TrabajoPracticoIntegrador-LUG-2B.sln en Visual Studio.
4. Restaurar paquetes NuGet si lo solicita Visual Studio.
5. Configurar:
   - Configuración: Debug
   - Plataforma: Any CPU / x86
6. Ejecutar con F5 (Debug) o Ctrl+F5 (sin depuración).

------------------------------------------------------------
ARQUITECTURA DEL PROYECTO
------------------------------------------------------------
UI (User Interface) - /UI
    Formularios y componentes gráficos.

BLL (Business Logic Layer) - /BLL
    Lógica de negocio y validaciones.

DAL (Data Access Layer) - /DAL
    Conexión y operaciones con base de datos.

------------------------------------------------------------
FLUJO DE TRABAJO CON GIT
------------------------------------------------------------
1. Crear rama nueva:
   git fetch origin
   git checkout -b feature/<descripcion>

2. Hacer cambios y subirlos:
   git add .
   git commit -m "feat(UI): agregar formulario de clientes"
   git push -u origin feature/<descripcion>

3. Crear Pull Request hacia main o develop en GitHub.

------------------------------------------------------------
CONVENCION PARA COMMITS
------------------------------------------------------------
Formato:
   <tipo>(<scope>): <descripcion>

Tipos comunes:
   feat: nueva funcionalidad
   fix: corrección de bug
   refactor: mejora sin cambio funcional
   docs: documentación
   chore: mantenimiento

Ejemplo:
   fix(DAL): corregir error de conexión a base de datos

------------------------------------------------------------
BUENAS PRACTICAS
------------------------------------------------------------
- No subir bin/, obj/, .vs/, *.exe, *.dll, *.user, *.suo
- Mantener las capas separadas
- No poner lógica de negocio en formularios
- Nombrar variables y métodos claramente
- Probar antes de cada commit y push

------------------------------------------------------------
DEBUG Y PRUEBAS
------------------------------------------------------------
- F5 para ejecutar en modo depuración.
- Si el diseñador WinForms falla:
    * Cerrar el form
    * Build -> Clean Solution
    * Build -> Rebuild Solution
- Revisar Output Window o Immediate Window.

------------------------------------------------------------
DEPENDENCIAS Y NUGET
------------------------------------------------------------
Restaurar paquetes automáticamente al abrir la solución.
Si falla:
   nuget restore TrabajoPracticoIntegrador-LUG-2B.sln

------------------------------------------------------------
RESOLUCION DE CONFLICTOS EN GIT
------------------------------------------------------------
1. Antes de subir cambios:
   git fetch origin
   git pull origin main
2. Resolver conflictos
3. Probar proyecto
4. Subir cambios:
   git add .
   git commit -m "merge: resolver conflictos con main"
   git push

------------------------------------------------------------
LICENCIA
------------------------------------------------------------
El proyecto está cubierto por la licencia incluida en el archivo LICENSE.

------------------------------------------------------------
EQUIPO
------------------------------------------------------------
Grupo LUG 2B - Trabajo Práctico Integrador
(Agregar nombres o usuarios de GitHub de los integrantes)

------------------------------------------------------------
ENLACES UTILES
------------------------------------------------------------
- Documentación C#: https://learn.microsoft.com/es-es/dotnet/csharp/
- Documentación .NET Framework: https://learn.microsoft.com/es-es/dotnet/framework/
- Guía Git y GitHub: https://docs.github.com/es
