# Branching en Git

## ¿Qué es una rama?

Una rama en Git es una línea de desarrollo independiente. Permite trabajar en nuevas funcionalidades o correcciones sin afectar el código principal.

## Comandos

### `git branch`

Lista todas las ramas locales del repositorio. La rama actual aparece marcada con un asterisco.

```bash
git branch
```

Para ver también las ramas remotas:

```bash
git branch -a
```

Para crear una nueva rama:

```bash
git branch nombre-de-la-rama
```

Para eliminar una rama:

```bash
git branch -d nombre-de-la-rama
```

---

### `git checkout`

Permite moverse entre ramas o restaurar archivos.

```bash
git checkout nombre-de-la-rama
```

Para crear una rama y moverse a ella al mismo tiempo:

```bash
git checkout -b nombre-de-la-rama
```

---

### `git switch`

Es el comando moderno para cambiar de rama (introducido en Git 2.23).

```bash
git switch nombre-de-la-rama
```

Para crear y moverse a una nueva rama:

```bash
git switch -c nombre-de-la-rama
```

---

### `git merge`

Une los cambios de otra rama a la rama actual.

```bash
git merge nombre-de-la-rama
```

---

### `git rebase`

Reaplica los commits de una rama sobre otra, generando un historial más limpio y lineal.

```bash
git rebase nombre-de-la-rama
```

---

## Conflictos al hacer merge
Cuando dos ramas modificaron el mismo archivo, Git no puede fusionarlas automáticamente y genera un conflicto. El archivo afectado queda marcado así:
