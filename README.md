# Trabajo Práctico de Metodología de Sistemas

Documentación de comandos, manejo de ramas, resolución de conflictos y extracción de estadísticas.
**Integrantes**:

- David Cardozo,
- Alejo Simos y
- Naim Neman.

# Stats

## Integrante con mayor cantidad de commits

<table>
<tr>
<th>COMANDO</th>
<th>SALIDA</th>
</tr>
<tr>
<td>

```bash
git shortlog -sn --all
```

</td>
<td>

```
12  Naim Neman
9   David Cardozo
7   Alejo Simos
```

</td>
</tr>
</table>

> Naim Neman realizó la mayor cantidad de commits, con un total de **12**.

---

## Cantidad total de merges

<table>
<tr>
<th>COMANDO</th>
<th>SALIDA</th>
</tr>
<tr>
<td>

```bash
git log --all --merges --oneline
```

</td>
<td>

```
345677e Merge pull request #4 from daviddcardozo2006/feature/branching-commands
667af9a Merge pull request #3 from daviddcardozo2006/feature/docs-merging
43369b3 Merge pull request #2 from daviddcardozo2006/feature/commits_commands
10cc376 Merge pull request #1 from daviddcardozo2006/feature/staging_commands
```

</td>
</tr>
</table>

> Se realizaron un total de **3** merges en el repositorio.

---

## Cantidad de conflictos producidos

// TODO

---

## Cantidad de ramas existentes en el repositorio

<table>
<tr>
<th>COMANDO</th>
<th>SALIDA</th>
</tr>
<tr>
<td>

```bash
git branch -r | grep -v HEAD | wc -l
```

</td>
<td>

```
  origin/develop
  origin/feature/branching-commands
  origin/feature/commits_commands
  origin/feature/docs-merging
  origin/feature/staging_commands
  origin/main
```

</td>
</tr>
</table>

---

## Commit con mayor cantidad de archivos modificados

<table>
<tr>
<th>COMANDO</th>
<th>SALIDA</th>
</tr>
<tr>
<td>

```bash
git log --all --shortstat --oneline
```

</td>
<td>

```
...
d5948e4 (origin/feature/branching-commands) fix: separar los comandos en archivos individuales
 6 files changed, 92 insertions(+), 90 deletions(-)
...
```

</td>
</tr>
</table>

> Cuando ejecutamos el comando adjunto buscamos en el listado de todos los commits aquel que tuvo la mayor cantidad de archivos modificados (files changed)

---

## Captura de un conflicto previo a su resolución, indicando el hash del commit asociado

// TODO
