## git mv

Mueve o renombra un archivo dentro del repositorio, conservando su historial de cambios.

### Manual

- `git mv {origen} {destino}`: _mueve o renombra el archivo_
- `git mv -f {origen} {destino}`: _mueve el archivo aunque el destino exista_

### Ejemplo

- **Situación:** `commit.md` fue commiteado por error en el directorio raíz y necesita moverse a `commits/`.

**`git mv commit.md commits/commit.md`**

<table>
<tr>
<th>ANTES</th>
<th>DESPUES</th>
</tr>
<tr>
<td>

```bash
$ git status
On branch feature/commits_commands
nothing to commit, working tree clean

$ ls
commit.md
commits/
staging/
```

</td>
<td>

```bash
$ git status
On branch feature/commits_commands
Changes to be committed:
  renamed: commit.md -> commits/commit.md

$ ls
commits/
staging/
```

</td>
</tr>
</table>

> A diferencia de hacer `mv` desde la terminal y luego `git add` por separado,
> `git mv` registra el movimiento como un _rename_ directamente, lo que
> Git usa para preservar el historial del archivo con `git log --follow`.
