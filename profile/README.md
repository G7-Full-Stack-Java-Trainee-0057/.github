# Flujo de Trabajo para Contribuciones
Bienvenido al documento que detalla el flujo de trabajo estándar para contribuciones a nuestro proyecto. Siguiendo estas pautas, aseguramos que cada contribución sea considerada y gestionada eficientemente.

## 1. Hacer Fork del Repositorio
Para empezar, realiza un fork del repositorio principal para tener tu propia copia en la que puedas trabajar:

- Navega al [repositorio original](https://github.com/G7-Full-Stack-Java-Trainee/M3-Bases_de_Datos) en GitHub.
- Haz clic en el botón **Fork** situado en la esquina superior derecha de la página.
![Fork](assets/images/fork-to-main-repo.png)


## 2. Clonar el Repositorio
Una vez que tengas el fork, clónalo para trabajar localmente en tu máquina:
![Clone UI](assets/images/clone-github-repo-for-vscode.png)

Puedes realizar el `git clone` a traves de la UI de VSCode.
![Clone Terminal](assets/images/git-clone.png)

Asi como tambien realizarlo a traves de la terminal.
```bash
git clone https://github.com/[nombre_de_usuario]/M3-Bases_de_Datos
```

Una vez clonado el repositorio en su espacio de trabajo confirme su posicion y acceda a el con la terminal:
```bash
ls
```
![Directories](assets/images/check-directories-files.png)

En caso de no estar en el directorio correcto acceda a el con `cd nombre_repo`:
```bash
cd [M3-Bases_de_Datos] // en este caso el repo es M3-Bases_de_Datos
```

## 3. Agrega el repositorio original como un remote.
Para mantener tu fork sincronizado con el repositorio original, añádelo como un remote llamado upstream:
```bash
git remote add upstream https://github.com/G7-Full-Stack-Java-Trainee/M3-Bases_de_Datos
```
![assign upstream](assets/images/assign-remote-branches-target.png)

Confirme que su `upstream` apunte a su fork
```bash
git remote -v
```
![check upstream direction](assets/images/check-direction-remote-branchs.png)

## 4. Sincronizar tu Fork (Actualiza su local en base a su remoto)
Actualizar tu Repositorio Local antes de trabajar para traer los últimos cambios del repositorio original (upstream) a tu repositorio local, utiliza:
```bash
git fetch upstream
```
![update main local](assets/images/update-main-branch-step1.png)

Cambiar a la Rama Principal
Asegúrate de estar en la rama principal, main, para aplicar los cambios:
```bash
git checkout main
```
![move to main](assets/images/move-to-main-branch.png)

Fusionar los Cambios
Finalmente, fusiona los cambios desde la rama principal del repositorio original a tu rama local `main`.
Este proceso actualiza tu rama main local con la última versión del main en el repositorio original.
```bash
git merge upstream/main
```
![update main local](assets/images/update-main-branch-step2.png)


# Haciendo Cambios

## 5. Crear una nueva rama
Crea una nueva rama basada en main para tus cambios, trabajar en una rama específica ayuda a mantener organizado tu trabajo y a separarlo de otros cambios concurrentes en el repositorio.:
```bash
git checkout -b [nombre_de_rama_de_trabajo]
```
![create work branch](assets/images/create-work-branch.png)


## 6. Realiza tus Cambios
Implementa tus cambios en la rama creada y realiza commits con mensajes explicativos:
```bash
git add .
git commit -m "Describe los cambios realizados"
```
![status branch before changes](assets/images/check-status-files-in-work-branch.png)
![add changes in work branch](assets/images/check-added-changes-in-work-branch.png)
![commit changes in work branch](assets/images/commit-changes-work-branch.png)

## 7. Confirma si tu rama main en github esta actualizada.
Permite tener actualizado el main en todo momento, confirma que estes en tu copia del repositorio. 
![check changes in main github](assets/images/update-github-branch-main-step1.png)

Si la rama se encuentra desactualizada, sincronizarla al ultimo estado.
![update changes in main github](assets/images/update-github-branch-main-step2.png)

## 8. Antes de enviar los cambios actualiza el main en local.
Desde tu VSCode actualiza el estado del main en local.
```bash
git checkout main
```
![move to main](assets/images/move-to-main-branch.png)

```bash
git fetch upstream
```
![update main local](assets/images/update-main-branch-step1.png)

```bash
git merge upstream/main
```
![update main local](assets/images/update-main-branch-step2.png)


## 9. Actualiza tu rama de trabajo antes de hacer efectivo el push.
Antes de enviar el cambio fusiona los cambios del main en tu rama de trabajo.
![update main local](assets/images/update-work-branch-local-before-push.png)
