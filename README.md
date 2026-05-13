# Test de Git
*Bienvenido a la guia rapidad de git*

# Crea un repositorio nuevo
Crea un directorio nuevo, ábrelo y ejecuta.
- git init

para crear un nuevo repositorio de git.

# Hacer checkout a un repositorio
Crea una copia local del repositorio ejecutando.
- git clone /path/to/repository

Si utilizas un servidor remoto, ejecuta.

- git clone username@host:/path/to/repository

# Add & Commit
Puedes registrar cambios (añadirlos al Index) usando:
- git add <filename>, index.html
- git add .

Este es el primer paso en el flujo de trabajo básico. Para hacer commit a estos cambios usa:
- git commit -m "Commit message"

Ahora el archivo esta incluído en el HEAD, pero aún no en tu repositorio remoto.

# Envío de cambios
Tus cambios están ahora en el HEAD de tu copia local. Para enviar estos cambios a tu repositorio remoto ejecuta:
- git push origin master

Reemplaza master por la rama a la que quieres enviar tus cambios.

Si no has clonado un repositorio ya existente y quieres conectar tu repositorio local a un repositorio remoto, usa:
- git remote add origin <server>

Ahora podrás subir tus cambios al repositorio remoto seleccionado.

# Ramas
Las ramas son utilizadas para desarrollar funcionalidades aisladas unas de otras. La rama master es la rama "por defecto" cuando creas un repositorio. Crea nuevas ramas durante el desarrollo y fusiónalas a la rama principal cuando termines.

Crea una nueva rama llamada "feature_x" y cámbiate a ella usando:
- git checkout -b feature_x

vuelve a la rama principal
- git checkout master

y borra la rama
- git branch -d feature_x

Una rama nueva no estará disponible para los demás a menos que subas (push) la rama a tu repositorio remoto
- git push origin <branch>