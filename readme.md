11) Deshacer el último commit (perdiendo los cambios realizados en el working copy) 
12) Rehacer el último commit (el que acabamos de deshacer) 
13) Hacer un merge con ‘main’ (styled absorbe a main)

- ¿Qué comando utilizaste en el paso 11? ¿Por qué? git reset --hard HEAD~ se utilizó el comando reset con --hard porque se quería perder los cambios realizados en el working copy y el HEAD~ deshace el último cambio.
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? Como ya tenía en el repositorio los cambios de la rama styled, cree la rama en mi local con git checkout -b styled y luego realicé un git pull origin styled y con eso tenía lo último de esa rama en el working copy.
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó conflicto porque styled fue creada a partir de main y main no ha cambiado su estado. 
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?-
Si creo conflicto, porque el contenido del archivo git-nuestro.md en la rama styled es distinto al contenido del archivo git-nuestro.md de la rama htmlify
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, porque el contenido de main no ha sido modificado, por lo tanto al hacer merge de styled, actualiza main con los cambios realizados en la rama styled.
- ¿Qué comando o comandos utilizaste en el paso 25?
git log --graph
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? Si, la diferencia es que con no fast forward no se muestra la historia de la rama title. 
- ¿Qué comando o comandos utilizaste en el paso 27? git reset HEAD~ no se utiliza el --hard porque sino se pierden los cambios del working copy

- ¿Qué comando o comandos utilizaste en el paso 28? git checkout main, para tener los cambios del repositorio y asì descartar los del working copy.
- ¿Qué comando o comandos utilizaste en el paso 29? 
git branch -d title 
- ¿Qué comando o comandos utilizaste en el paso 30?
Primero usé: git checkout title para crear de nuevo la rama title. Luego usé git log --graph para ver el commit que tenía el cambio del título. seguidamente use git reset HEAD más el HASH del commit con el título.verifique que el cambio del título estuviera en mi Working copy usando cat git-nuestro.mdAl verificar que estaba el cambio, me moví a la rama main usando git checkout mainY desde main hice de nuevo un git merge main
32) Volver al commit inicial cuando se creó el poema git log --graph para ver el hash del commit inicial, luego git reset HEAD HASH del commit inicial33) Volver al estado final, cuando pusimos título al poema
git log --graph para ver el hash del title, luego reset HEAD HASH del commit del titulo
