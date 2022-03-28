# Notas Git



## reset

### Primero
`git reset --hard a1fbd68ce149387afe8d2cabb80ff678c9f9fc0c`   // Cortamos todo hasta ese commit, volvemos literalmente atras

`git reset --hard HEAD~1`  // Tambien puede ser este comando y es un commit hacia atras,  `HEAD~2` seria dos.

### Segundo
`git push --force`   // Forzamos a que estos cambios se reflejen en el repositorio remoto

### Tercero
si un tercer repositorio está 'clonado' y mantenido vía pull desde ese repositorio cuando queramos actualizar mediante `git pull` no hara mucho. Solo marcara que en `origen` el HEAD y el main estan en un commit anterior, para modificarlo y llevarlo hasta ese mismo punto debemos usar tambien en el `git reset --hard a1fbd68ce149387afe8d2cabb80ff678c9f9fc0c`

## revert


## commit --amend
Cambiar mensaje de ultimo commit
`git commit --amend -m "your new message"`


