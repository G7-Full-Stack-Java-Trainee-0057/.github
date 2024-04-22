# Flujo de Trabajo para Contribuciones

Bienvenido al documento que detalla el flujo de trabajo estándar para contribuciones a nuestro proyecto. Siguiendo estas pautas, aseguramos que cada contribución sea considerada y gestionada eficientemente.

## Configuración Inicial
Antes de comenzar a contribuir, asegúrate de configurar tu entorno de desarrollo correctamente.

### 1. Hacer Fork del Repositorio

Para empezar, realiza un fork del repositorio principal para tener tu propia copia en la que puedas trabajar:

- Navega al [repositorio original](https://github.com/G7-Full-Stack-Java-Trainee/M3-Bases_de_Datos) en GitHub.
- Haz clic en el botón **Fork** situado en la esquina superior derecha de la página.
![Fork](https://github.com/G7-Full-Stack-Java-Trainee/assets/images/fork-example.png)


### 2. Clonar el Repositorio

Una vez que tengas el fork, clónalo para trabajar localmente en tu máquina:

```bash
git clone https://github.com/G7-Full-Stack-Java-Trainee/M3-Bases_de_Datos
```
![Fork](https://github.com/G7-Full-Stack-Java-Trainee/assets/images/clone-section.png)

### 3. Agrega el repositorio original como un remote

Para mantener tu fork sincronizado con el repositorio original, añádelo como un remote llamado upstream:

```bash
git remote add upstream https://github.com/[nombre_del_usuario]/M3-Bases_de_Datos.git
```

### 4. Sincronizar tu Fork

Antes de comenzar a trabajar en cambios nuevos, sincroniza tu fork:

```bash
git fetch upstream
```

Este comando se utiliza para actualizar tu repositorio local con los cambios del original (upstream)

```bash
git checkout main
```

Este comando asegura que todos los merges o cambios que realices sean aplicados en la rama `main`.

```bash
git merge upstream/main
```
Este proceso actualiza tu rama main local con la última versión del main del repositorio original.

## Haciendo Cambios

### 5. Crear una nueva rama

Crea una nueva rama basada en main para tus cambios:

```bash
git checkout -b develop
```

Trabajar en una rama específica ayuda a mantener organizado tu trabajo y a separarlo de otros cambios concurrentes en el repositorio.

### 6. Realiza tus Cambios

Implementa tus cambios en la rama creada y realiza commits con mensajes explicativos:

```bash
git add .
git commit -m "Describe los cambios realizados"
```

### 7. Publicar la Rama en GitHub

Cuando estés listo para obtener feedback sobre tus cambios, sube la rama a tu fork en GitHub:

```bash
git push origin nombre-rama
```

## Enviando un Pull Request

### 8. Crear un Pull Request

Desde tu fork en GitHub, puedes enviar un pull request:

- Ve a la página del repositorio en GitHub y selecciona tu rama.
- Haz clic en `New pull request`.
- Revisa los cambios, asegúrate de que estás comparando la rama correcta del repositorio original y tu rama de cambios.
- Haz clic en `Create pull request`.

### 9. Revisión y Merge del Pull Request

Espera a que los mantenedores del proyecto revisen tu pull request. Si es necesario, podrían pedirte que realices modificaciones. Una vez aprobado, ellos harán merge de tus cambios al repositorio principal.

# Verificación Post-Push

Después de hacer push, es una buena práctica verificar que todo está correcto:

```bash
git status
git log
```
