# Git Commands 🧑‍💻

## 🛠️ Comandos básicos de Git

### Comandos con abreviación de palabra (`-`) y con palabra completa (`--`)

- `-` : Comando con abreviación de palabra
- `--` : Comando con palabra completa

---

### 📜 Comandos Útiles

#### `code`

🖥️ Abre Visual Studio Code (VS Code) desde la terminal.

#### `git --help`

Muestra ayuda para el comando `git`. Útil para obtener detalles de cualquier comando en Git.

#### `git config --global init.defaultBranch main`

Configura la rama principal como `main` para cada nuevo repositorio inicializado. Esto asegura que cada repositorio tenga `main` como rama principal por defecto.

#### `git init`

Inicializa un nuevo repositorio en la carpeta actual.

## ➕ git add

#### `git add ComandosDeGit.txt`

📂 Agrega el archivo `ComandosDeGit.txt` al área de espera (staging area) para ser preparado antes de subirlo al repositorio.

#### `git add .`

📁 Agrega **todos los archivos** de la carpeta actual al área de espera para su próximo commit.

## ✅ git commit

#### `git commit -m "Mensaje"`

📤 Realiza un commit con el mensaje especificado, subiendo los archivos del área de espera al repositorio.

#### `git commit -am "Mensaje"`

📝 Añade los cambios al commit, combinando `git add .` y el commit clásico. **Nota**: Este comando no funcionará si los archivos nunca han sido agregados previamente con `git add`.

#### `git commit --amend`

🔄 Reagrupa los cambios en el commit anterior, permitiendo que se envíen todos en un único commit.

## git status

#### `git status`

🔍 Permite verificar qué archivos están en el área de espera (staging area) y cuáles han sido modificados pero aún no agregados.

## git show

#### `git show`

📜 Muestra todos los cambios realizados en el último commit.

#### `git show archivo`

📄 Muestra los cambios específicos que se han hecho en un archivo determinado.

## git log

#### `git log ComandosDeGit.txt`

📜 Muestra el historial de cambios de un archivo específico, en este caso `ComandosDeGit.txt`.

#### `git log --stat`

📊 Permite ver los cambios específicos realizados en cada archivo a partir de un commit.

#### `git log --all --graph`

🌲 Muestra una representación gráfica de cómo se han gestionado y desarrollado las ramas en el repositorio.

#### `git log --all --graph --decorate --oneline`

📋 Muestra todas las ramas del repositorio de forma resumida, con una vista compacta y decorada.

#### `alias jamon="$ git log --all --graph --decorate --oneline"`

🔗 Asigna un alias al comando largo para facilitar su escritura y ejecución. En este caso, el alias `jamon` permite ejecutar el comando de una manera más rápida.

## git rm

#### `git rm historia.txt`

❌ Elimina el archivo `historia.txt` del área de espera (staging area) y lo marca para ser eliminado en el próximo commit.

#### `git rm --cached historia.txt`

📁 Elimina el archivo `historia.txt` del área de espera, pero **lo mantiene en el disco duro**. Esto es útil si deseas dejar de rastrear un archivo sin eliminarlo físicamente.

#### `git rm --force`

🗑️ Elimina el archivo de Git y del disco duro. Este comando forzará la eliminación, pero el archivo aún puede recuperarse a partir de versiones anteriores si el commit fue registrado.

## Configuración de usuario en Git 🛠️

#### `git config`

📜 Muestra una lista de todas las configuraciones actuales que tiene Git.

#### `git config --list`

📋 Muestra la configuración por defecto de tu Git y los parámetros que le faltan.

#### `git config --list --show-origin`

📍 Muestra la ubicación de las configuraciones guardadas (directorios) en tu sistema.

#### `git config --global user.name "Tu Nombre"`

👤 Cambia la configuración del nombre de usuario a nivel global, aplicable a todos los repositorios en tu máquina.

#### `git config --global user.email "Tu Correo"`

📧 Cambia la configuración del correo electrónico a nivel global, aplicable a todos los repositorios en tu máquina.

## Comandos de Vim y salida de commits 🖥️

#### `Esc + Shift + ZZ`

🚪 Fuerza el envío de commits que no llevan un mensaje.

#### `Q`

🔙 Permite salir de los comandos cuando el contenido mostrado es muy extenso.

## git diff

#### `git diff commitA commitB`

🔍 Compara las diferencias entre dos versiones del archivo. **Recomendación**: Coloca la versión más antigua primero (`commitA`) y la más nueva después (`commitB`). Es aconsejable hacer un `git log` previamente, ya que el nombre del commit es una combinación de letras y números que aparece en esa lista.

## Comandos para traer cambios y manejar ramas 📦

#### `git checkout`

🔄 Trae los últimos cambios o los que desees de ciertos archivos.

#### `git checkout nombrerama`

🌿 Cambia de una rama a otra especificada por `nombrerama`.

#### `git switch nombrerama`

🔄 Alternativa para cambiar de una rama a otra especificada por `nombrerama`.

#### `git checkout -b nombrerama`

✨ Crea una nueva rama (`nombrerama`) y cambia directamente a ella.

#### `git checkout versioncommit Nombrearchivo`

📄 Trae los cambios de un archivo específico de una versión de commit determinada.

#### `git checkout master Nombrearchivo`

📥 Trae la versión actual del archivo desde la rama `master` en el repositorio.

## git revert y reset

### Comandos para revertir y resetear cambios 🔄

#### `git revert commit numerosdelcommit`

↩️ Revierte los cambios de un commit anterior, creando un nuevo commit que indica que se realizó una reversión del commit especificado.

#### `git reset versionanterior --hard`

🛑 Restaura todo a una versión anterior del repositorio, eliminando los cambios actuales. **¡Cuidado!**: Se pierden los cambios no guardados.

#### `git reset versionanterior --mixed`

🚮 Elimina todos los commits y también borra los cambios del área de staging, dejando el directorio de trabajo intacto.

#### `git reset versionanterior --soft`

🔄 Restaura a una versión anterior del repositorio, manteniendo los cambios en el área de staging para que se puedan volver a comprometer.

#### `git reset HEAD`

📥 Saca los archivos del área de staging, regresándolos al estado de no rastreado.

## Comandos para trabajar con repositorios remotos 🌐

#### `git clone url`

🔄 Clona el repositorio desde la URL proporcionada, trayendo una copia del `master` y de todos los directorios del repositorio en GitHub.

#### `git push origin`

📤 Envía todos los cambios y commits que se encuentran almacenados localmente en Git al repositorio remoto.

#### `git fetch`

🔄 Trae los cambios del repositorio remoto y los almacena en el repositorio local, **sin modificar** los archivos en tu directorio de trabajo.

#### `git merge`

🔗 Combina los archivos actuales de tu repositorio con los cambios traídos desde el repositorio remoto.

#### `git pull origin`

⬇️ Combinación de `git fetch` y `git merge`, que actualiza tu rama local con los cambios más recientes del repositorio remoto.

## Comandos para manejar ramas en Git 🌿

#### `git branch nombre`

🌱 Crea una nueva rama con el nombre especificado.

#### `git branch -m nuevonombre`

✏️ Cambia el nombre de la rama en la que te encuentras actualmente a `nuevonombre`.

#### `git branch --list`

📋 Muestra una lista de todas las ramas existentes en el repositorio.

#### `git branch --delete nombrerama`

🗑️ Elimina la rama especificada por `nombrerama`.

#### `git branch -D nombrerama`

🚨 Fuerza la eliminación de la rama especificada, incluso si no ha sido fusionada.

#### `git branch -v`

📜 Muestra el último commit de cada rama existente.

#### `git branch --merged`

🔄 Lista las ramas que han sido fusionadas con la rama actual.

#### `git branch --no-merged`

❌ Lista las ramas que **no** se han fusionado con la rama actual.

#### `git branch -r`

🌍 Muestra las ramas remotas del repositorio.

#### `git branch -a`

🌐 Muestra todas las ramas, tanto locales como remotas.

## git merge

### Comandos para fusionar ramas en Git 🔄

#### `git merge nombrarama`

🔗 Une los cambios de `nombrarama` con la rama actual (se debe realizar desde la rama principal). **Nota**: Puedes incluir un "mensaje opcional" para describir el merge.

#### `git merge --abort`

⏸️ Anula el proceso de merge y restaura el estado anterior, deshaciendo cualquier cambio realizado durante el merge.

### Resolución de conflictos al hacer un merge ⚠️

Cuando unificas cambios, puede haber conflictos. Si esto ocurre, deberás decidir cuál parte del código conservar y cuál descartar. Asegúrate de revisar cada conflicto cuidadosamente antes de finalizar el merge.

## Llaves públicas y llaves privadas (cifrado asimétrico de un solo camino) 🔐

1. **Abrir Git Bash**
   - Asegúrate de estar en la carpeta home de tu PC usando el comando:

     ```bash
     pwd
     ```

2. **Generar una llave SSH**
   - Ejecuta el siguiente comando para crear una nueva llave SSH:

     ```bash
     ssh-keygen -t rsa -b 4096 -C "perezrestrepoalejandro9@gmail.com"
     ```

   - Esto generará la llave y te pedirá que elijas dónde guardarla. Es recomendable hacerlo en la carpeta home.
   - También se te pedirá que ingreses una contraseña; puedes optar por poner una o dejarla en blanco.

3. **Agregar la llave al entorno o sistema operativo**
   - Para asegurarte de que el sistema reconozca la llave, revisa el servidor de llaves con el siguiente comando:

     ```bash
     eval $(ssh-agent -s)
     ```

4. **Agregar la llave privada al sistema**
   - Añade la llave privada a tu sistema o servidor con el comando:

     ```bash
     ssh-add ~/.ssh/id_rsa
     ```

5. **Verificar la conexión con GitHub**
   - Establece una conexión SSH con GitHub para comprobar que todo esté funcionando correctamente:

     ```bash
     ssh -T git@github.com
     ```

## Relacionar tus credenciales SSH con GitHub 🔗

1. **Acceder a tu perfil de GitHub**
   - Dirígete a tu perfil y selecciona **Settings** (Configuraciones).

2. **Agregar una nueva llave SSH**
   - En el apartado de **SSH and GPG keys**, haz clic en **New SSH key** (Crear nueva llave SSH).
   - Pega tu llave pública en el campo proporcionado y guarda los cambios.

3. **Agregar un repositorio remoto**
   - Para vincular un repositorio con tu carpeta local, utiliza el siguiente comando:

     ```bash
     git remote add origin url
     ```

   - Sustituye `url` con la URL de tu repositorio.

4. **Verificar los repositorios remotos**
   - Para mostrar los enlaces a los que puedes hacer push y pull, ejecuta:

     ```bash
     git remote -v
     ```

## Establecer la rama principal como `main` 🌟

1. **Renombrar la rama actual a `main`**
   - Ejecuta el siguiente comando para cambiar el nombre de la rama actual a `main`:

     ```bash
     git branch -m main
     ```

2. **Traer datos del repositorio remoto y subir los cambios**
   - Para obtener los datos del repositorio remoto y fusionar con la rama local, usa:

     ```bash
     git pull origin main
     ```

3. **Configurar el comportamiento de `pull`**
   - Configura Git para que no utilice rebase al hacer pull:

     ```bash
     git config pull.rebase false
     ```

4. **Permitir la fusión de historias no relacionadas**
   - Si es necesario, permite la fusión de historias no relacionadas al hacer pull:

     ```bash
     git pull origin main --allow-unrelated-histories
     ```

5. **Subir cambios al repositorio remoto**
   - Finalmente, sube los cambios de tu rama local `main` al repositorio remoto:

     ```bash
     git push origin main
     ```

## Poner tags a los commits 🏷️

1. **Crear un tag para la versión actual**
   - Ejecuta el siguiente comando para crear un tag en la versión actual del proyecto:

     ```bash
     git tag nombretag
     ```

2. **Crear un tag para un commit específico**
   - Para crear un tag anotado en un commit específico, utiliza el siguiente comando:

     ```bash
     git tag -a v=0.1 -m "Primeras clases" numerosdelcommit
     ```

   - Reemplaza `numerosdelcommit` con el identificador del commit al que deseas asociar el tag.

3. **Mostrar una lista de todos los tags**
   - Para ver todos los tags existentes en el repositorio, ejecuta:

     ```bash
     git tag
     ```

4. **Mostrar los tags y sus commits relacionados**
   - Para visualizar los tags y el commit al que están asociados, utiliza:

     ```bash
     git show-ref --tags
     ```

## Enviar y eliminar tags en GitHub 🚀

1. **Enviar tags a GitHub**
   - Para enviar todos los tags que has creado a GitHub, utiliza el siguiente comando:

     ```bash
     git push origin --tags
     ```

2. **Eliminar un tag del entorno local**
   - Para eliminar un tag de tu repositorio local, ejecuta:

     ```bash
     git tag -d nombreTag
     ```

   - Reemplaza `nombreTag` con el nombre del tag que deseas eliminar.

3. **Eliminar un tag de GitHub**
   - Para eliminar un tag de GitHub, utiliza el siguiente comando:

     ```bash
     git push origin :refs/tags/nombreTag
     ```

   - Asegúrate de reemplazar `nombreTag` con el nombre del tag que deseas eliminar.

## Enviar diferentes branches a GitHub 🌿

1. **Mostrar la lista de branches actuales**
   - Para ver la lista de branches que existen en tu repositorio, ejecuta:

     ```bash
     git show-branch
     ```

2. **Mostrar la lista de branches de manera más específica**
   - Para obtener una vista más detallada de todos los branches, utiliza:

     ```bash
     git show-branch --all
     ```

3. **Abrir la aplicación para visualizar branches y commits**
   - Usa el siguiente comando para abrir una aplicación que te permita ver los branches y todos los commits:

     ```bash
     gitk
     ```

4. **Enviar una rama a GitHub**
   - Para enviar la rama actual a GitHub, utiliza:

     ```bash
     git push origin nombrebranch
     ```

5. **Subir commits de la rama y la rama a GitHub**
   - Para subir los commits de una rama y establecer el upstream para futuras referencias, ejecuta:

     ```bash
     git push -u origin nombrebranch
     ```

6. **Crear un nuevo branch**
   - Para crear un nuevo branch llamado `header`, usa:

     ```bash
     git branch header
     ```

7. **Crear otro nuevo branch**
   - Para crear otro branch llamado `footer`, utiliza:

     ```bash
     git branch footer
     ```

8. **Traer una rama específica del repositorio**
   - Para obtener una rama específica del repositorio, ejecuta:

     ```bash
     git pull origin nombrerama
     ```

## Pull Requests 🛠️

En entornos reales de programación, los merges con la rama `main` son revisados y deben pasar por un proceso de validación.

### Hacer un Pull Request después de realizar un merge desde otra rama al `main`

1. **Acceder a la sección de Pull Requests**
   - Dirígete a la pestaña de **Pull Requests** en tu repositorio y selecciona **New Pull Request** o simplemente haz clic en el banner que aparecerá al ingresar al repositorio.

2. **Seleccionar ramas para comparar**
   - En la interfaz, escoge la rama que deseas comparar con tu rama `main`.

3. **Agregar revisores**
   - Puedes agregar a otras personas para que revisen tu Pull Request y te brinden retroalimentación.

4. **Revisión de cambios**
   - Desde la vista de quien está revisando, se puede hacer clic en **Review Changes**. Aquí pueden:
     - Aprobar el merge.
     - Pedir cambios.
     - Dejar un comentario.

5. **Realizar cambios requeridos**
   - Si se solicitan cambios, realiza las modificaciones necesarias en tu código. Luego, haz un nuevo `push` para enviar los cambios.

6. **Revisar nuevamente**
   - Después de enviar los cambios, el Pull Request puede ser aceptado o denegado nuevamente.

## Creando un Fork 🍴

Un **fork** es tomar una copia del estado actual de un proyecto y clonarlo se hace desde github.

### Hacer un Pull desde un Fork

1. **Agregar el repositorio original como remoto:**

   ```bash
   git remote add upstream https://github.com/AlejandroPR23/Curso-Profesional-de-Git-y-Github.git
   ```

   Esto agrega el repositorio original como un remoto, permitiéndote hacer pulls desde él. El nombre asignado en este caso es **upstream**.

2. **Realizar un Pull del repositorio original:**

   ```bash
   git pull upstream origin
   ```

   Este comando trae los cambios del repositorio original hacia tu fork.

> **Nota:** Todo este proceso también se puede realizar directamente desde GitHub.

### Tener un Servidor Local desde NPM 🌐

Para crear un servidor local, sigue estos pasos:

1. **Instalar http-server de forma global:**

   ```bash
   npm install --global http-server
   ```

2. **Iniciar el servidor:**

   ```bash
   http-server
   ```

   Esto iniciará el servidor en tu máquina local.

## Ignorar Archivos en el Repositorio con `.gitignore` 🚫

Para ignorar archivos en tu repositorio, sigue estos pasos:

1. **Crear un archivo llamado `.gitignore`:**
   Dirígete a tu carpeta del proyecto y crea un archivo llamado `.gitignore`.

2. **Agregar tipos de archivos a ignorar:**
   Dentro del archivo `.gitignore`, puedes especificar los tipos de archivos que Git debería ignorar. Por ejemplo:

   ```plaintext
   *.jpg   # Ignorar todos los archivos .jpg
   *.jpeg  # Ignorar todos los archivos .jpeg
   ```

   Puedes añadir más extensiones o patrones según sea necesario.

## README.md es una Excelente Práctica 📖

El archivo `README.md` es fundamental para tu repositorio, ya que:

- **Informa al mundo sobre el propósito de tu repositorio.** 🌍
- **Permite agregar contenido en Markdown y HTML al mismo tiempo.** 🛠️
- **Se puede editar fácilmente desde Visual Studio Code o en MEditor.md.** ✏️

Asegúrate de incluir detalles relevantes como la descripción del proyecto, instrucciones de instalación, uso y cualquier otra información que pueda ser útil para los usuarios.

## Sitio Web Público con GitHub Pages 🌐

Sigue estos pasos para crear un sitio web público usando GitHub Pages:

1. Abre [pages.github.com](https://pages.github.com).
2. Crea un nuevo repositorio con el nombre: `tu-usuario.github.io`.
3. Clona el repositorio:

   ```bash
   git clone url-repositorio
   ```

4. Crea un nuevo archivo `index.html` y cambia el nombre de la carpeta principal a `docs`.
5. Haz el push al repositorio:

   ```bash
   git push origin main
   ```

6. Ve a la configuración del repositorio (`Settings`), busca `Pages` y elige el branch del cual desplegarás el `index.html`.
7. Ahora dirígete a tu página en: `https://tu-usuario.github.io` y ¡listo! 🎉
8. **Extra:** [Crea una página personalizada de error 404 para GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/creating-a-custom-404-page-for-your-github-pages-site).

## Rebase en Git ⚙️

**Nota:** El uso de rebase en repositorios remotos es considerado una mala práctica. Se recomienda realizarlo únicamente en repositorios locales.

### Pasos para realizar un rebase

1. Crea una nueva rama:

   ```bash
   git checkout -b nueva-rama
   ```

2. Realiza los cambios que desees en esa rama.

3. Estando en la rama creada, ejecuta:

   ```bash
   git rebase main
   ```

4. En caso de que haya problemas de unión (conflictos), puedes resolverlos y continuar con el siguiente comando:

   ```bash
   git rebase --continue
   ```

5. Cambia a la rama principal:

   ```bash
   git checkout main
   ```

6. Finalmente, fusiona la rama rebased con la principal:

   ```bash
   git rebase nueva-rama
   ```

Ahora las dos ramas se habrán fusionado correctamente.

## Git Stash 🗄️

Imagina que quieres cambiar de rama y no deseas hacer un commit de tus cambios actuales, pero quieres guardarlos temporalmente. Esto se hace con `git stash`.

### Comandos de Git Stash

1. **Guardar cambios del archivo actual temporalmente:**

   ```bash
   git stash
   ```

2. **Guardar todos los cambios de todos los archivos:**

   ```bash
   git stash -u
   ```

3. **Guardar los cambios temporalmente con un nombre específico:**

   ```bash
   git stash save "mensaje"
   ```

4. **Mostrar la lista de cambios guardados temporalmente:**

   ```bash
   git stash list
   ```

5. **Crear una nueva rama y aplicar el stash:**

   ```bash
   git branch nombrerama stash@(<num_stash>)
   ```

6. **Liberar los cambios guardados para hacer el commit (se pueden liberar en cualquier rama):**

   ```bash
   git stash pop
   ```

7. **Liberar un cambio específico:**

   ```bash
   git stash pop stash@(<num_stash>)
   ```

8. **Eliminar el último cambio agregado a la lista de cambios guardados:**

   ```bash
   git stash drop
   ```

9. **Eliminar un stash específico:**

   ```bash
   git stash drop stash@(<num_stash>)
   ```

10. **Eliminar toda la lista de stashes:**

    ```bash
    git stash clear
    ```

## Git Clean 🧹

El comando `git clean` se utiliza para eliminar archivos que no deberían estar en el repositorio, es decir, aquellos que no están bajo seguimiento por Git.

### Comandos de Git Clean

1. **Revisar qué archivos no tienen seguimiento y serán eliminados:**

   ```bash
   git clean --dry-run
   ```

   *Este paso es obligatorio y debe hacerse primero para evitar la eliminación accidental de archivos importantes.*

2. **Eliminar los archivos que no son mostrados por el comando anterior:**

   ```bash
   git clean
   ```

3. **Eliminar los archivos forzadamente (usar si el comando anterior no funciona):**

   ```bash
   git clean -f
   ```

## Git Cherry-Pick 🍒

El comando `git cherry-pick` se utiliza para traer cambios desde otra rama a la rama actual. Sin embargo, se considera mala práctica abusar de este comando.

### Comandos de Git Cherry-Pick

1. **Traer un commit específico de otra rama a la rama principal:**

   ```bash
   git cherry-pick nombrecommitdelaotraram
   ```

   *Este comando traerá el commit de la otra rama a la rama actual, conservando su nombre original.*

2. **Traer los cambios del commit sin ejecutar el commit:**

   ```bash
   git cherry-pick nombrecommitdelaotraram -n
   ```

   *Con la opción `-n`, se aplican los cambios, pero no se realiza un nuevo commit.*

3. **Cambiar el nombre del commit al traerlo:**

   ```bash
   git cherry-pick nombrecommitdelaotraram -e "Cambio"
   ```

   *Con la opción `-e`, puedes modificar el mensaje del commit al aplicarlo.*

## Crear un Issue Template 📝

Para mejorar la gestión de problemas en tu repositorio de GitHub, puedes crear una plantilla para reportar errores. Aquí te explico cómo hacerlo:

### Pasos para crear un Issue Template

1. **Crear una carpeta `.github` en tu repositorio local.**

   ```bash
   mkdir .github
   ```

2. **Dentro de la carpeta `.github`, crea otra carpeta llamada `ISSUE_TEMPLATE`.**

   ```bash
   mkdir .github/ISSUE_TEMPLATE
   ```

3. **Crea un archivo llamado `bug_report.md`.**

   ```bash
   touch .github/ISSUE_TEMPLATE/bug_report.md
   ```

4. **Agrega una plantilla para ingresar errores en el archivo `bug_report.md`.**

   ```markdown
   # Reporte de Error

   **Descripción del error:**
   [Describe brevemente el error]

   **Pasos para reproducir:**
   1. [Paso 1]
   2. [Paso 2]
   3. [Paso 3]

   **Resultado esperado:**
   [Describe el resultado que esperabas]

   **Resultado actual:**
   [Describe lo que realmente sucedió]

   **Información adicional:**
   [Agrega cualquier otra información relevante, como capturas de pantalla o detalles del entorno]
   ```

5. **Ve a la pestaña de "Issues" en tu repositorio en GitHub y encontrarás la plantilla disponible.**

6. **Puedes agregar más plantillas para otros tipos de errores creando archivos adicionales en la carpeta `ISSUE_TEMPLATE`.**

## Crear un Pull Request Template 📄

Para facilitar la creación y revisión de Pull Requests en tu repositorio, puedes establecer una plantilla. A continuación, te explico cómo hacerlo:

### Pasos para crear un Pull Request Template

1. **Accede a la carpeta `.github` en tu repositorio local.**

   ```bash
   cd .github
   ```

2. **Crea un archivo llamado `pull_request_template.md`.**

   ```bash
   touch pull_request_template.md
   ```

3. **Agrega el contenido de la plantilla al archivo `pull_request_template.md`.**

   ```markdown
   # Pull Request Template

   **Descripción:**
   [Proporciona una breve descripción de los cambios realizados]

   **Motivación y contexto:**
   [Explica la razón detrás de estos cambios]

   **Tipo de cambio:**
   - [ ] Bug fix
   - [ ] Nueva característica
   - [ ] Cambio de documentación
   - [ ] Otros (especificar)

   **Cómo probar estos cambios:**
   [Proporciona instrucciones sobre cómo probar los cambios]

   **Capturas de pantalla:**
   [Incluye capturas de pantalla si es necesario]

   **Checklist:**
   - [ ] He probado mis cambios
   - [ ] He documentado mis cambios
   - [ ] Mis cambios no rompen nada
   ```

## GitHub Projects 🛠️

Para organizar tareas y colaborar de manera más eficiente, puedes utilizar la funcionalidad de GitHub Projects. Aquí te muestro cómo hacerlo:

1. **Ingresa a [GitHub.com](https://github.com).**

2. **Dirígete al módulo de "Projects" en tu repositorio.**

3. **Al dar clic en "Crear", se te mostrarán diversas plantillas para aplicar a tu proyecto.**

4. **Dependiendo de la plantilla que elijas, podrás organizar cada tarea y asignarla a alguien.**

5. **Vincular proyecto y repositorio:**
   - Al lado del "draft", haz clic en los tres puntos (⋮).
   - Selecciona "Convertir en issue" y elige un proyecto específico.

## Mejorar archivos `.md` con Markdownlint 📝

Para hacer que tus archivos Markdown sean más limpios y mejor estructurados, puedes seguir estos pasos:

1. **Instala la extensión de Markdownlint** en tu editor de código (por ejemplo, Visual Studio Code).

2. **Vista previa de archivos Markdown:**
   - Desde el ícono de cuadro con lupa en la parte superior derecha de Visual Studio Code, puedes ver la vista previa de tus archivos `.md`.

---

## Herramienta para hacer diagramas de trabajo de ramas en GitHub: Mermaid 🌊

Mermaid es una herramienta excelente para crear diagramas de flujo y gráficos de trabajo en Git. Sigue estos pasos para crear un diagrama de trabajo de ramas:

1. **Ir a Mermaid:** Accede a [Mermaid](https://mermaid-js.github.io/mermaid-live-editor).

2. **Dirígete a "Mermaid Live":** Esto te llevará al editor en línea donde puedes escribir y visualizar tus diagramas.

3. **Ingresa el siguiente código para crear un gráfico de Git:**

   ```mermaid
   gitGraph:
       commit
       branch develop
       checkout develop
       commit
       checkout main
       merge develop
       commit
   ```

4. **Palabras clave que puedes usar:**
   - `commit`: Crea un nuevo commit en la rama actual.
   - `branch`: Crea una nueva rama.
   - `checkout`: Cambia a la rama especificada.
   - `merge`: Combina la rama especificada con la actual.

Esto te permitirá visualizar mejor el flujo de trabajo y las interacciones entre las ramas en tu proyecto.

### Personalizar tu GitHub 🎨

Para darle un toque personal a tu perfil de GitHub, sigue estos pasos:

1. **Crea un repositorio con el nombre de tu usuario:**
   - El nombre del repositorio debe ser exactamente igual a tu nombre de usuario en GitHub (por ejemplo, `tu_usuario`).

2. **Crea un archivo `README.md`:**
   - Este archivo servirá como la presentación de tu repositorio y perfil.

3. **Personaliza el `README.md`:**
   - Agrega información sobre ti, tus proyectos, habilidades y cualquier otra cosa que quieras compartir. Usa Markdown para darle formato.

---

## GitHub Wikis 📚

Las Wikis en GitHub te permiten crear una documentación más estructurada para tus repositorios. Aquí te explico cómo hacerlo:

1. **Accede a la opción de Wiki:**
   - Dirígete a tu repositorio y busca la pestaña de **Wiki** en la parte superior.

2. **Crea un nuevo Wiki:**
   - Haz clic en **Crear Wiki** para iniciar tu documentación.

3. **Agrega más páginas:**
   - Puedes crear múltiples páginas dentro de tu Wiki para organizar mejor la información.

4. **Crea una barra lateral:**
   - Utiliza una página de índice para crear una barra lateral que facilite la navegación entre las páginas de tu Wiki.

5. **Sé creativo:**
   - Personaliza el contenido, agrega imágenes, enlaces y cualquier otro recurso que ayude a comunicar tu mensaje de manera efectiva.

¡Ahora tienes un perfil de GitHub más personalizado y una documentación organizada para tus proyectos!

## GitHub Gist 📝

GitHub Gist es una manera sencilla de compartir fragmentos de código que no necesitan estar ligados a algún repositorio. Sigue estos pasos para crear y compartir un Gist:

1. **Visita la página de Gist:**
   - Dirígete a [gist.github.com](https://gist.github.com).

2. **Crea un nuevo Gist:**
   - Allí podrás poner tu fragmento de código, darle un título y, si lo deseas, especificar el tipo de archivo.

3. **Copia la URL del Gist:**
   - Una vez creado, copia la URL de tu Gist y compártela con tus compañeros.

4. **Discute sobre tu Gist:**
   - Ahora puedes tener una charla sobre el fragmento de código compartido con tu compañero.

5. **Edita y elimina:**
   - Puedes editar tu fragmento de código directamente en la página y eliminarlo si lo deseas.

¡Así de fácil es compartir código con GitHub Gist!

## Automatizar GitHub Projects ⚙️

Para facilitar la gestión de tus proyectos en GitHub, puedes automatizar ciertas tareas siguiendo estos pasos:

1. **Accede a GitHub Projects:**
   - Dirígete a tu proyecto en GitHub.

2. **Selecciona opciones de automatización:**
   - Haz clic en los tres puntos al lado de "Insights" y elige "Workflows".

3. **Configura la automatización:**
   - Allí podrás elegir varias secciones que te ayudarán a automatizar la gestión del proyecto. (Para obtener más detalles, es recomendable profundizar en **GitHub Actions**).

4. **Cierra tareas automáticamente:**
   - Al hacer un pull request, puedes incluir la palabra `closes #` seguida del número de la tarea que deseas cerrar.

¡Con estas configuraciones, podrás optimizar la gestión de tus proyectos en GitHub!

## GitHub Codespaces (Ambientes de trabajo en la nube) ☁️

GitHub Codespaces permite crear ambientes de desarrollo en la nube para facilitar tu trabajo. Sigue estos pasos para empezar:

1. **Crear un Codespace:**
   - Dirígete al botón donde puedes crear un repositorio y selecciona la opción de **Crear un Codespace**.

2. **Configura tu Codespace:**
   - Selecciona el repositorio que deseas utilizar, la rama principal, tu región horaria y el tipo de máquina en la nube.

3. **Usa tu Codespace:**
   - Ahora podrás trabajar sin problemas en tu Codespace.

4. **Elimina tu Codespace:**
   - Es importante que elimines tu Codespace una vez que concluyas tu actividad para liberar recursos.

5. **Utiliza plantillas:**
   - Puedes utilizar plantillas de Codespaces que facilitan el trabajo según lo que elijas (React, Django, Python, etc.).

6. **Instala Live Share:**
   - Descarga **Live Share** para trabajar en la nube junto con otros.

7. **Colabora con compañeros:**
   - Envía el enlace a un compañero y podrán hacer **pair programming** juntos.

¡Aprovecha GitHub Codespaces para optimizar tu flujo de trabajo en la nube!

## GitHub.dev (Editor en línea) ✏️

GitHub.dev te permite editar tu código directamente desde tu navegador. Sigue estos pasos:

1. **Abre el editor:**
   - Al presionar la tecla **","** o la tecla **"."** en cualquier repositorio, se abrirá un editor tipo Visual Studio Code.

2. **Edita tu código:**
   - Ahora podrás editar tu código de forma sencilla y rápida.

¡Aprovecha GitHub.dev para realizar cambios rápidos en tus proyectos sin necesidad de clonar el repositorio!

## Repositorios Privados y el Uso de Tokens 🔐

1. **Crear un Repositorio Privado:**
   - Comienza creando un nuevo repositorio y selecciona la opción de **privado**.

2. **Acceder a la Configuración de Tokens:**
   - Ve a **Settings** y luego a **Developer settings** (es el último en la lista de ajustes).

3. **Generar un Token:**
   - Busca la sección de **tokens** y elige **classic tokens**.
   - Haz clic en **Generate new token**.
   - Asegúrate de copiar el token generado y elegir los permisos necesarios, ya que no podrás volver a verlo después de salir de la página.

4. **Tokens Fine-Grained:**
   - También existen los **fine-grained tokens**, que ofrecen un control más detallado sobre los permisos. El proceso de creación es similar.

5. **Clonar Repositorios Privados:**
   - Al intentar clonar el repositorio privado en otro PC, se te pedirá una contraseña. En este caso, debes usar el token que generaste como contraseña.

## Dependabot (Actualización Automática de Packages) 🔄

1. **Acceder a Configuraciones:**
   - Ve a **Settings** o a **Security** dentro de tu repositorio.

2. **Activar Dependabot:**
   - Busca la sección de **Dependabot** y activa todas las opciones seleccionando la opción de **Dependabot version updates**.

3. **Configuración del Archivo .yml:**
   - Aparecerá un archivo `.yml` donde podrás configurar Dependabot.

4. **Personalización de Configuración:**
   - En este archivo, podrás especificar cómo quieres que Dependabot revise paquetes específicos, la frecuencia de las revisiones, entre otras configuraciones.

## Gestión de Datos Sensibles y Políticas de Seguridad 🔒

La gestión de datos sensibles y la implementación de políticas de seguridad son esenciales para proteger la integridad de tu código y la información sensible en GitHub. Aquí te explicamos cómo hacerlo de manera efectiva.

#### 1. Acceder a Ajustes

- Dirígete a la página principal de tu repositorio en GitHub.
- Haz clic en la pestaña **"Settings"** (Ajustes), que se encuentra en la parte superior de la página.
- En la barra lateral izquierda, desplázate hacia abajo y selecciona **"Code Security and Analysis"**.

#### 2. Habilitar Code Scanning

- En la sección de **Code Security and Analysis**, busca el apartado de **Code Scanning**.
- Selecciona **CodeQL Analysis**. Este análisis está diseñado para buscar vulnerabilidades en tu código y sugerir correcciones.
- Asegúrate de habilitarlo en **Default** para que se ejecute automáticamente con cada push y pull request.
  - **Configuración adicional:** Puedes personalizar el comportamiento de CodeQL a través de un archivo de configuración `.yml`, donde puedes especificar qué lenguajes de programación analizar y cómo manejar los hallazgos.

#### 3. Activar Secret Scanning

- Una vez habilitado el análisis de CodeQL, se activará automáticamente el **Secret Scanning**. Este escáner revisa tu código en busca de credenciales o datos sensibles (como claves API, contraseñas, etc.) que no deberían estar en el repositorio.
- Si se detectan secretos, recibirás alertas para que puedas tomar las medidas necesarias, como rotar las credenciales comprometidas y eliminar el secreto del repositorio.
  
#### 4. Configuración de Alertas y Respuestas

- En la misma sección, puedes configurar las notificaciones para alertas relacionadas con vulnerabilidades y secretos.
- Es recomendable establecer un flujo de trabajo para responder rápidamente a las alertas, asegurando que se tomen medidas inmediatas ante cualquier detección de datos sensibles.

#### 5. Mejores Prácticas

- **Revisión del Código:** Implementa un proceso de revisión de código para asegurar que los cambios propuestos sean revisados antes de ser fusionados.
- **Uso de Variables de Entorno:** Evita almacenar datos sensibles en el código fuente. Utiliza variables de entorno o servicios de gestión de secretos para manejar credenciales y otros datos sensibles.
- **Auditoría Regular:** Realiza auditorías periódicas de tu código y de las configuraciones de seguridad para identificar y mitigar posibles riesgos.

#### 6. Recursos Adicionales

- Para más información sobre cómo gestionar secretos en GitHub, visita la [documentación oficial de GitHub sobre la gestión de secretos](https://docs.github.com/en/actions/security-guides/encrypted-secrets).
- Considera implementar herramientas adicionales de seguridad como Dependabot para mantener tus dependencias actualizadas y seguras.

Al seguir estos pasos, puedes mejorar la seguridad de tu repositorio y proteger los datos sensibles de tu proyecto. Mantener una buena higiene de seguridad es fundamental para el éxito y la integridad de cualquier proyecto de software.

## Administración de Repositorios y Organizaciones en GitHub 👥

La administración de repositorios y organizaciones es fundamental para facilitar la colaboración y la gestión de proyectos en GitHub. Aquí te explicamos cómo crear y administrar una organización, así como las mejores prácticas para la gestión de repositorios.

#### 1. Crear una Nueva Organización

- **Acceso a la Opción de Creación:**
  - Inicia sesión en tu cuenta de GitHub.
  - Haz clic en el botón **"+"** (más) ubicado en la esquina superior derecha de la página.
  - Selecciona **"New organization"** (Nueva organización) del menú desplegable.

- **Elegir un Plan:**
  - Se te presentarán diferentes planes para organizaciones (gratuito, pago, etc.). Selecciona el que mejor se adapte a tus necesidades. Los planes pagos ofrecen características adicionales como mayor almacenamiento, opciones de seguridad avanzadas y más.

- **Proporcionar Información de la Organización:**
  - Completa los campos requeridos, incluyendo el nombre de la organización, la dirección de correo electrónico y otros detalles pertinentes.
  - Puedes agregar participantes iniciales que deseas que formen parte de la organización desde el principio.

#### 2. Finalizar la Creación de la Organización

- Una vez que hayas ingresado toda la información requerida, haz clic en el botón **"Create organization"** (Crear organización).
- GitHub procesará tu solicitud y creará la organización.

#### 3. Pasos Recomendados para Configurar tu Organización

- Después de crear la organización, GitHub te presentará una serie de pasos recomendados en seis recuadros. Estos pasos te ayudarán a configurar adecuadamente tu organización:
  
  1. **Configurar el Perfil de la Organización:**
     - Completa la información de perfil, incluyendo una descripción de la organización y su logotipo.

  2. **Invitar a Miembros:**
     - Agrega más miembros a tu organización, asignando roles y permisos apropiados según sus responsabilidades.

  3. **Crear Repositorios:**
     - Empieza a crear repositorios para tus proyectos dentro de la organización. Puedes elegir entre repositorios públicos o privados.

  4. **Establecer Equipos:**
     - Configura equipos dentro de la organización para facilitar la colaboración. Asigna permisos de acceso a diferentes repositorios según el equipo.

  5. **Definir Políticas de Seguridad:**
     - Configura políticas de seguridad para proteger tu organización y sus repositorios. Esto incluye habilitar la autenticación de dos factores (2FA) y gestionar los permisos de acceso.

  6. **Configurar GitHub Actions (opcional):**
     - Si deseas automatizar flujos de trabajo, configura GitHub Actions para integraciones y despliegues continuos.

#### 4. Mejores Prácticas para la Administración de Repositorios

- **Organización de Repositorios:**
  - Utiliza nombres claros y descriptivos para tus repositorios.
  - Crea un archivo `README.md` en cada repositorio para documentar el propósito y uso del proyecto.

- **Colaboración Efectiva:**
  - Fomenta el uso de **Pull Requests** para revisar cambios propuestos antes de fusionarlos en la rama principal.
  - Utiliza **Issues** para rastrear errores y tareas pendientes, asegurando que todos estén al tanto del progreso del proyecto.

- **Auditoría y Seguridad:**
  - Realiza auditorías periódicas de los permisos de acceso y la actividad en los repositorios.
  - Establece políticas claras sobre la gestión de datos sensibles y el uso de herramientas de análisis de seguridad.

Al seguir estos pasos, podrás administrar tu organización en GitHub de manera efectiva, facilitando la colaboración y la gestión de proyectos de manera segura y estructurada.

## Personalizar tu Perfil de GitHub con GitHub Actions 🎨

Personalizar tu perfil de GitHub puede hacer que se vea más atractivo y profesional. Una forma de hacerlo es mediante el uso de GitHub Actions para mostrar actividad en tu perfil. A continuación, te explicamos cómo hacerlo paso a paso:

#### 1. Elegir el Repositorio de tu Nombre

- **Crea un Repositorio:**
  - Asegúrate de que tienes un repositorio con el nombre exacto de tu usuario de GitHub (por ejemplo, si tu usuario es `usuario`, el repositorio debe llamarse `usuario`).
  - Si no lo tienes, crea un nuevo repositorio con tu nombre de usuario.

#### 2. Editar el `README.md`

- **Abrir el Archivo README:**
  - En tu repositorio, localiza y abre el archivo `README.md`.

- **Agregar Secciones de Actividad:**
  - Dentro del archivo `README.md`, añade el siguiente código entre comentarios:

    ```markdown
    <!-- START_SECTION:activity -->
    <!-- END_SECTION:activity -->
    ```

  - Estas etiquetas indican dónde se insertará la actividad de GitHub en tu perfil.

#### 3. Configurar GitHub Actions

- **Ir a la Pestaña de GitHub Actions:**
  - En tu repositorio, haz clic en la pestaña **"Actions"**.

- **Elegir un Workflow Sencillo:**
  - Selecciona un workflow sencillo para empezar. GitHub proporciona algunas plantillas predefinidas que puedes usar.

- **Escribir el Código del Workflow:**
  - Necesitarás configurar un archivo YAML en `.github/workflows/` para automatizar la actualización de la sección de actividad. Aquí hay un ejemplo básico de lo que podría contener tu archivo:

    ```yaml
    name: Update Activity
    on:
      schedule:
        - cron: '0 * * * *' # Actualiza cada hora
    jobs:
      update:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout
            uses: actions/checkout@v2
          - name: Update activity
            uses: crazy-max/ghaction-github-actions@v1
            with:
              GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
    ```

  - Este archivo cron se ejecutará según la programación que establezcas. En este caso, se actualizará cada hora.

#### 4. Ejecutar GitHub Actions

- **Ejecutar el Workflow:**
  - Después de configurar tu archivo YAML, vuelve a la pestaña de **"Actions"** en tu repositorio.
  - Encuentra tu workflow y haz clic en el botón **"Run workflow"** para ejecutarlo manualmente por primera vez.

#### 5. Verificar la Personalización

- **Visitar tu Perfil:**
  - Después de que tu GitHub Action haya terminado de ejecutarse, ve a tu perfil de GitHub.
  - Deberías ver la sección de actividad actualizada en tu `README.md` según la configuración que hayas realizado.

### Consideraciones Finales

- **Explorar Más Opciones:**
  - Puedes personalizar aún más tu perfil utilizando diferentes acciones y configuraciones en tu workflow. Explora la [Marketplace de GitHub Actions](https://github.com/marketplace?type=actions) para encontrar acciones que se ajusten a tus necesidades.

- **Ajustes Adicionales:**
  - No dudes en modificar el cron o agregar otros pasos a tu workflow para incluir información adicional que desees mostrar en tu perfil.

Al seguir estos pasos, podrás personalizar tu perfil de GitHub y mostrar tu actividad de manera dinámica y atractiva.

## GitHub CLI (gh) 🖥️

GitHub CLI es una herramienta de línea de comandos que te permite interactuar con GitHub desde tu terminal. Facilita la gestión de repositorios, problemas, pull requests y más sin necesidad de utilizar la interfaz web. A continuación, te explicamos cómo instalarlo y algunos de los comandos más útiles.

#### 1. Instalación de GitHub CLI

- **Visitar el Repositorio de GitHub CLI:**
  - Dirígete al [repositorio oficial de GitHub CLI](https://github.com/cli/cli) para obtener la información de instalación.

- **Instalación:**
  - Dependiendo de tu sistema operativo, sigue las instrucciones proporcionadas. Puedes instalarlo usando un gestor de paquetes o descargando directamente el binario.

#### 2. Comandos Básicos de GitHub CLI

A continuación se presentan algunos comandos útiles que puedes utilizar con GitHub CLI:

- **Crear un Nuevo Repositorio:**

  ```bash
  gh repo create
  ```

  - Este comando crea un nuevo repositorio en GitHub. Te guiará a través de una serie de preguntas para configurar el nombre, la visibilidad (público o privado) y otros ajustes.

- **Crear un Nuevo Issue:**

  ```bash
  gh issue create
  ```

  - Este comando te permite crear un nuevo issue para el repositorio en el que te encuentres. Puedes especificar el título, la descripción y otras opciones desde la línea de comandos.

#### 3. Otros Comandos Útiles

Para explorar más comandos disponibles en GitHub CLI, puedes consultar la documentación oficial:

- **Documentación Completa de GitHub CLI:**
  - [Manual de GitHub CLI](https://cli.github.com/manual/)

Algunos comandos adicionales que podrías encontrar útiles incluyen:

- **Listar Issues:**

  ```bash
  gh issue list
  ```

- **Ver Detalles de un Issue:**

  ```bash
  gh issue view <issue_number>
  ```

- **Crear un Pull Request:**

  ```bash
  gh pr create
  ```

### Consideraciones Finales

- **Configuración Inicial:**
  - Asegúrate de configurar tu cuenta de GitHub con `gh auth login` para autenticarte y acceder a tus repositorios.

- **Integración con Otras Herramientas:**
  - GitHub CLI se puede utilizar junto con otras herramientas de desarrollo y scripts para automatizar flujos de trabajo.

Con GitHub CLI, puedes gestionar tus proyectos y colaborar con otros de manera más eficiente directamente desde la terminal.

## Creación y Publicación de un Paquete de Python con GitHub Releases 🚀

#### 1. Crear el archivo `setup.py`

El archivo `setup.py` es fundamental para definir la información y la estructura de tu paquete. Crea un archivo llamado `setup.py` en la raíz de tu proyecto con el siguiente contenido:

```python
from setuptools import setup, find_packages

setup(
    name="mi_paquete",                            # Nombre del paquete
    version="0.0.1",                             # Versión inicial
    packages=find_packages(),                     # Paquetes a incluir
    description="Un paquete pip simple de saludo",  # Breve descripción
    author="Tu Nombre",                           # Tu nombre
    author_email="tu_email@example.com",         # Tu correo electrónico
    url="https://github.com/tu_usuario/mi_repositorio",  # URL del proyecto
)
```

#### 2. Crear la estructura de carpetas

Crea una carpeta con el mismo nombre que tu paquete. Dentro de esta carpeta, crea un archivo llamado `__init__.py` que será el módulo principal de tu paquete. La estructura de tu proyecto debería verse así:

```
mi_proyecto/
│
├── setup.py
└── mi_paquete/
    ├── __init__.py
```

#### 3. Agregar contenido al archivo `__init__.py`

Dentro del archivo `__init__.py`, puedes definir las funciones o clases que desees que tu paquete exponga. Por ejemplo:

```python
def saludar(nombre):
    return "Hola " + nombre + ", este es mi primer paquete pip!"
```

#### 4. Crear el paquete

Abre tu terminal, navega a la raíz de tu proyecto y ejecuta el siguiente comando para crear el paquete:

```bash
python3 setup.py bdist_wheel sdist
```

Esto generará archivos `.whl` y `.tar.gz` en una carpeta llamada `dist`, que contienen tu paquete listo para ser distribuido.

#### 5. Crear un nuevo Release en GitHub

1. Ve a tu repositorio en GitHub.
2. Haz clic en la pestaña "Releases".
3. Haz clic en "Draft a new release".

#### 6. Crear un Tag (Versión)

- En la sección "Tag version", escribe la versión de tu paquete, por ejemplo, `v0.0.1`.
- Asegúrate de que el tag siga el formato `vX.Y.Z`, donde `X`, `Y`, y `Z` son números que representan la versión.

#### 7. Publicar el Release

1. Sube los archivos que generaste en la carpeta `dist` a este nuevo release. Puedes arrastrarlos y soltarlos en la interfaz de GitHub.
2. Escribe una descripción del release si lo deseas.
3. Haz clic en "Publish release" para hacer público tu paquete.

#### 8. Instalar el paquete usando pip

Una vez que hayas publicado tu paquete, otros usuarios podrán instalarlo usando `pip` directamente desde tu repositorio de GitHub:

```bash
pip install git+https://github.com/tu_usuario/mi_repositorio.git
```

### Consideraciones Finales

- **Pruebas**: Antes de publicar tu paquete, asegúrate de probarlo localmente para verificar que todo funcione como se espera.
- **Documentación**: Es recomendable incluir documentación sobre cómo usar tu paquete, ya sea en el README del repositorio o en un archivo separado.
- **Versionado**: Sigue buenas prácticas de versionado (semántico) para facilitar el mantenimiento y la actualización de tu paquete.

Con estos pasos, habrás creado y publicado con éxito un paquete de Python en GitHub. ¡Buena suerte!

## Git Reset y Reflog

## 1. Git Reset

`git reset` se utiliza para deshacer cambios en el área de staging y en el directorio de trabajo. Hay diferentes modos de uso:

### a. `git reset --soft`

- **Descripción**: Este comando mueve el puntero HEAD a la referencia anterior, pero mantiene los cambios en el área de staging (index).
- **Uso**:

    ```bash
    git reset --soft <commit>
    ```

### b. `git reset --hard`

- **Descripción**: Este comando restablece el puntero HEAD a la referencia anterior y elimina todos los cambios en el área de staging y en el directorio de trabajo. **(Mala práctica en muchas situaciones, ya que elimina cambios no guardados)**
- **Uso**:

    ```bash
    git reset --hard <commit>
    ```

## 2. Git Reflog

`git reflog` es una herramienta útil que permite ver un registro de todas las referencias y cambios realizados en tu repositorio, incluso aquellos que han sido eliminados.

### Descripción

- **Función**: Muestra todos los cambios hechos hasta ahora, incluyendo las actualizaciones de ramas y los cambios eliminados, enumerados por referencia.
- **Uso**:

    ```bash
    git reflog
    ```

### Ejemplo de salida

Al ejecutar `git reflog`, obtendrás una salida que muestra una lista de acciones recientes en tu repositorio:

```
1d2a3b4 HEAD@{0}: commit: Mensaje del commit
5c6d7e8 HEAD@{1}: reset: moving to HEAD^
9f0a1b2 HEAD@{2}: checkout: moving from branch to branch
```

Esto te permitirá regresar a un estado anterior de tu proyecto si es necesario, utilizando la referencia mostrada.

## Consideraciones Finales

- **Precaución con `--hard`**: Ten cuidado al usar `git reset --hard`, ya que puede llevar a la pérdida de trabajo no guardado.
- **Uso de `reflog`**: Es recomendable revisar el `reflog` si necesitas deshacer cambios o recuperar un estado anterior del repositorio.

Con esta guía, deberías tener una comprensión clara de cómo usar `git reset` y `git reflog` de manera efectiva en tus proyectos.

## Git Grep y Log

## 1. Git Grep

`git grep` es una herramienta que permite buscar patrones en el contenido de los archivos de tu repositorio.

### a. Buscar una palabra

- **Comando**:

    ```bash
    git grep palabra
    ```

- **Descripción**: Busca en todos los archivos del repositorio la palabra especificada y muestra un resumen de los archivos donde se encuentra.

### b. Buscar una palabra con número de línea

- **Comando**:

    ```bash
    git grep -n palabra
    ```

- **Descripción**: Similar al anterior, pero también muestra el número de línea donde aparece la palabra en cada archivo.

### c. Contar la cantidad de ocurrencias

- **Comando**:

    ```bash
    git grep -c palabra
    ```

- **Descripción**: Cuenta la cantidad de veces que la palabra aparece en los archivos. Este comando también funciona con etiquetas HTML.

## 2. Git Log

`git log` permite explorar el historial de commits de un repositorio.

### a. Buscar palabra específica en commits

- **Comando**:

    ```bash
    git log -S palabra
    ```

- **Descripción**: Busca una palabra específica en el contenido de los commits. Solo muestra los commits que añaden o eliminan esa palabra.

### b. Buscar palabras en mensajes de commits

- **Comando**:

    ```bash
    git log --all --grep=palabra
    ```

- **Descripción**: Busca la palabra en los mensajes de commit a través de todas las ramas. Muestra todos los commits cuyo mensaje contenga la palabra especificada.

## Consideraciones Finales

- **Usabilidad**: `git grep` es útil para localizar rápidamente contenido en el código, mientras que `git log` ayuda a revisar el historial de cambios y entender la evolución del proyecto.
- **Combinación de comandos**: Puedes combinar estas herramientas para obtener una visión más completa de cómo y dónde se usa una palabra o frase específica en tu proyecto.

Con esta guía, deberías poder usar `git grep` y `git log` de manera efectiva para buscar información relevante en tu repositorio.

## Comandos y Recursos Colaborativos de Git

## 1. Git Shortlog

El comando `git shortlog` se utiliza para generar un resumen de los commits por autor.

### a. Mostrar commits por miembro del grupo

- **Comando**:

    ```bash
    git shortlog -sn
    ```

- **Descripción**: Muestra cuántos commits ha hecho cada miembro del grupo.

### b. Mostrar commits por miembro sin contar merges

- **Comando**:

    ```bash
    git shortlog -sn --all --no-merges
    ```

- **Descripción**: Muestra la cantidad de commits por cada miembro, excluyendo los merges.

## 2. Git Blame

El comando `git blame` permite identificar quién realizó cambios en cada línea de un archivo específico.

### a. Ver quién hizo cada línea en un archivo

- **Comando**:

    ```bash
    git blame archivo
    ```

- **Descripción**: Muestra línea por línea quién hizo cada cambio en un archivo específico.

### b. Ver quién hizo cada línea con mejor indentación

- **Comando**:

    ```bash
    git blame -c archivo
    ```

- **Descripción**: Similar al anterior, pero con mejor indentación para facilitar la lectura.

### c. Ver quién hizo cada línea en un rango específico

- **Comando**:

    ```bash
    git blame archivo -L lineinicial,lineafinal
    ```

- **Descripción**: Muestra quién hizo cada cambio línea por línea en un rango específico (ejemplo: L35,L60).

## Consideraciones Finales

- **Colaboración**: Estos comandos son esenciales para entender la contribución de cada miembro del equipo y para facilitar la revisión de cambios en el código.
- **Aprendizaje continuo**: Familiarizarse con herramientas como Jenkins, Azure, GitLab y DevOps puede mejorar significativamente tus habilidades en la gestión de proyectos de software.

Con esta guía, podrás utilizar comandos colaborativos en Git y explorar nuevas herramientas para mejorar tu flujo de trabajo.

## GRACIAS 🥰
