# git rebase

Reaplica los commits de una rama sobre otra, generando un historial más limpio y lineal a diferencia del merge.

## Uso básico

```bash
git rebase nombre-de-la-rama
```

## Diferencia con merge

- `merge` conserva el historial completo con todos los commits de ambas ramas.
- `rebase` reescribe el historial colocando tus commits al final de la rama base, como si hubieras empezado a trabajar desde ahí.