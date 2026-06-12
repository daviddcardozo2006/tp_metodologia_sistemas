# git merge

Une los cambios de otra rama a la rama en la que estás parado actualmente.

## Uso básico

```bash
git merge nombre-de-la-rama
```

## Conflictos

Cuando dos ramas modificaron el mismo archivo, Git no puede fusionarlas automáticamente y marca el conflicto así:
<<<<<<< HEAD
tu código