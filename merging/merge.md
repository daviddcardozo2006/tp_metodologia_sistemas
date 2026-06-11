## Git Merge

### Concepto
El comando `merge` trae los cambios de otra rama hacia la rama actual. Su objetivo es integrar el historial sin alterar lo que ya existe.

### Comportamiento Arquitectónico
* Cuando se ejecuta, Git crea un nuevo commit de merge.
* La historia mantiene la bifurcación original de las ramas.
* Es un proceso seguro porque no se reescriben commits previos.

### Ventajas y Desventajas
* **Ventajas:** No modifica la historia existente. Es el método más seguro para el trabajo colaborativo en equipo.
* **Desventajas:** Genera una historia más compleja visualmente si hay múltiples ramas activas.

### Sintaxis y Ejemplo
Para traer los cambios de `main` hacia tu rama actual (`feature`):

```bash
git checkout feature
git merge main
```