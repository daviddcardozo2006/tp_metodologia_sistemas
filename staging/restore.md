## git restore

Descarta los cambios del _working directory_ ó saca archivos del _staging area_, restaurándolos al estado del último _commit_.

### Manual

- `git restore {file}`: _descarta cambios en el working directory_
- `git restore --staged {file}`: _saca el archivo del staging area **sin descartar los cambios**_
- `git restore --staged --worktree {file}`: _combina los efectos de los comandos anteriores_

### Ejemplo

- **Situación**: Modificamos "README.md" y lo agregamos al staging. Luego nos dimos cuenta que los cambios tenian errores y queremos deshacerlo.
  > En ¹ buscamos descartar los cambios del staging area pero no buscamos descartar los cambios permanentemente; en ² no nos importa perder los cambios efectuados.

¹ **`git restore --staged README.md`**

<table>
<tr>
<th>ANTES</th>
<th>DESPUÉS</th>
</tr>
<tr>
<td>

```bash
$ git status
Changes to be committed:
  modified: README.md
```

</td>
<td>

```bash
$ git status
Changes not staged for commit:
  modified: README.md
```

</td>
</tr>
</table>

² **`git restore README.md`**

<table>
<tr>
<th>ANTES</th>
<th>DESPUÉS</th>
</tr>
<tr>
<td>

```bash
$ git status
Changes not staged for commit:
  modified: README.md
```

</td>
<td>

```bash
$ git status
nothing to commit, working tree clean
```

</td>
</tr>
</table>
