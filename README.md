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
    14  David
    14  naimneman99
    10  alesi753
```

</td>
</tr>
</table>

> Tanto David como Naim realizaron la mayor cantidad de commits, con un total de **14** cada uno.
> Igualmente, hay una diferencia entre los commits locales y los del repositorio en Github que pueden visualizar dentro de Github Insights.

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
git log --all --merges --oneline | grep Merge
```

</td>
<td>

```
af4edb7 Merge pull request #8 from daviddcardozo2006/develop
a3f6c3f Merge branch 'develop' into staging_branch
08c3698 Merge pull request #6 from daviddcardozo2006/feature/staging_commands
d1d6a96 Merge pull request #5 from daviddcardozo2006/feature/indice
345677e Merge pull request #4 from daviddcardozo2006/feature/branching-commands
667af9a Merge pull request #3 from daviddcardozo2006/feature/docs-merging
43369b3 Merge pull request #2 from daviddcardozo2006/feature/commits_commands
10cc376 Merge pull request #1 from daviddcardozo2006/feature/staging_commands
```

</td>
</tr>
</table>

> Se realizaron un total de **8** merges en el repositorio.

---

## Cantidad de conflictos producidos

> Se forzó y resolvió 1 conflicto a la hora de señalar el mismo archivo staging/mv.md desde dos ramas. Donde a la hora de
> cometer el PR dentro de Github el auto-merge falló. Luego hubieron dos alternativas, editar las lineas de texto conflictivas
> del archjivo y luego mergear o simplemente descartar el PR. Por simplicidad fuimos con la segunda opción.

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
git branch -r | grep -v HEAD
```

</td>
<td>

```
  origin/develop
  origin/feature/branching-commands
  origin/feature/commits_commands
  origin/feature/docs-merging
  origin/feature/indice
  origin/feature/staging_commands
  origin/main
  origin/staging_branch
```

</td>
</tr>
</table>

> La cantidad de ramas existentes es de **8**.

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

<table>
<tr>
<th>COMANDO</th>
<th>SALIDA</th>
</tr>
<tr>
<td>

```bash
git log --graph --oneline --all -n 5
```

</td>
<td>

```
* 1d912 (HEAD -> feature/indice, origin/feature/indice) fix: resolver colision de sincronizacion en indice
|\
| * 31818 docs: inyectar arbol
| 2c987 feat: inyectar arbol grafico
|/
820bf docs: generar indices de modulos
```

</td>
</tr>
</table>

> Evidencia de colisión en el entorno de desarrollo: Intentamos generar el índice de archivos y módulos del repositorio. Al correr el comando, los nodos 31818 y 2c987 colisionaron y el merge automático falló, por lo que tuvimos que resolverlo a mano. El commit resultante quedó registrado con el hash 1d912.
