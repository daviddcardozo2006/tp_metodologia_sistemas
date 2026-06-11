## git commit

Guarda los cambios del _staging area_ en el historial del repositorio como un nuevo _commit_.
Podríamos decir que le "sacamos una foto" al estado actual de los archivos para registrarlos.

### Manual

- `git commit`: _crea un commit de los archivos modificados_
- `git commit -m "{mensaje}"`: _crea un commit con su mensaje descriptivo_
- `git commit --amend`: _modifica el último commit (mensaje o contenido)_
- `git commit --amend --no-edit`: _agrega cambios al último commit sin modificar el mensaje_

### Ejemplo

- **Situación**: Tenemos "README.md" en staging y hacemos el commit.

**`git commit -m "docs: update README"`**

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
nothing to commit, working tree clean

$ git log --oneline -1
a3f9c2b docs: update README
```

</td>
</tr>
</table>

> Los mensajes deben seguir la convención _conventional commits_:
> `tipo(scope): descripción` — ej: `feat:`, `fix:`, `docs:`, `style:`.
