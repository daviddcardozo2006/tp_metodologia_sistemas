## Git Rebase

### Concepto
A diferencia del merge, `rebase` mueve la base de la rama actual hacia otra rama.

### Comportamiento Arquitectónico
* Los commits de tu rama se reaplican uno por uno sobre la rama destino.
* Al hacer esto, el sistema genera nuevos commits con nuevos hashes.
* El resultado es que la historia queda completamente lineal. La rama base (ej. `main`) no cambia.

### Resolución de Conflictos
Si hay colisiones de código, Git pausa el rebase en el commit problemático. El desarrollador debe decidir el resultado final manualmente. Una vez editado el archivo, se continúa el proceso:

```bash
# Agregar la resolución al area de staging
git add archivo.txt
# Continuar aplicando el resto de los commits
git rebase --continue
```