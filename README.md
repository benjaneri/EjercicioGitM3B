# Ejercicio de Branching en Git y Resolución de Conflictos

En este ejercicio, simularemos un flujo de trabajo normal utilizando ramificaciones en Git. Además, enfrentaremos y resolveremos conflictos durante la fusión de ramas.

## Paso 0: Configuración inicial

Primero, asegúrate de tener Git instalado en tu sistema.

Hacer un fork de este repositorio.
![image](https://github.com/benjaneri/EjercicioGitM3B/assets/89653970/c84d002b-9c35-465b-a419-54e705e17966)


Luego, clonar el fork del repositorio en tu máquina local para comenzar a trabajar.

## Paso 1: Crear una nueva rama

Primero, vamos a crear una nueva rama llamada `nueva-funcionalidad` desde la rama principal (main).

## Paso 2: Realizar cambios en la nueva rama

Ahora nos movemos a la nueva rama y vamos a agregar una nueva característica a nuestra aplicación de gestión de tareas. En el archivo `tareas.js` dentro de la carpeta `src` implementaremos la lógica para agregar nuevas tareas.

```javascript
class GestorTareas {
    constructor() {
        this.tareas = [];
    }

    agregarTarea(tarea) {
        // Lógica para agregar una nueva tarea
        this.tareas.push({
            tarea: tarea,
            completada: false,
        });
        console.log("Nueva tarea agregada:", tarea);
    }

    obtenerTareas() {
        return this.tareas;
    }
}
```

También actualizaremos el archivo `funcionalidades.md` para incluir información sobre esta nueva característica.

```markdown
# Aplicación de Gestión de Tareas

Esta es una aplicación simple para gestionar tus tareas diarias.

## Características

-   Agregar nuevas tareas
-   Marcar tareas como completadas
-   Visualizar lista de tareas
```

## Paso 3: Confirmar los cambios en la nueva rama

Después de realizar los cambios, confirmaremos nuestras modificaciones en la nueva rama.

## Paso 4: Publicar la rama

Publicar la rama en el repositorio remoto.

## Paso 5: Crear una nueva rama desde la rama principal

Ahora, vamos a crear una nueva rama llamada `otra-funcionalidad` desde la rama principal (main).

## Paso 6: Realizar cambios en la nueva rama

Simulemos que otro desarrollador ha realizado cambios en el archivo `tareas.js`, agregando una validación adicional para las nuevas tareas.

```javascript
class GestorTareas {
    constructor() {
        this.tareas = [];
    }

    agregarTarea(tarea) {
        if (tarea.trim() !== "") {
            // Lógica para agregar una nueva tarea
            this.tareas.push({
                tarea: tarea,
                completada: false,
            });
            console.log("Nueva tarea agregada:", tarea);
        } else {
            console.error("La tarea no puede estar vacía");
        }
    }

    obtenerTareas() {
        return this.tareas;
    }
}
```

## Paso 7: Confirmar los cambios en la nueva rama y publicar la rama

Confirmaremos los cambios en la nueva rama y publicaremos la rama en el repositorio remoto.

## Paso 8: Fusionar la rama `nueva-funcionalidad` con la rama principal

Ahora, intentaremos fusionar la rama `nueva-funcionalidad` con la rama principal.

## Paso 9: Fusionar la rama `otra-funcionalidad` con la rama principal

Después de fusionar la rama `nueva-funcionalidad`, intentaremos fusionar la rama `otra-funcionalidad` con la rama principal. Para así quedarnos con las últimas modificaciones.

## Paso 9: Resolver conflictos

Durante la fusión, surgirá un conflicto debido a los cambios conflictivos en el mismo archivo `tareas.js`. Abriremos el archivo en conflicto y resolveremos manualmente el conflicto.

Después de resolver el conflicto, realizar el commit confirmando la fusión.

## Paso 10: Subir los cambios fusionados

Finalmente, subiremos los cambios fusionados a nuestro repositorio remoto.
