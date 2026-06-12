## git add

Agrega archivos nuevos o modificados del _working area_ al _staging area_ para incluirlos en un próximo _commit_.

### Manual

- `git add {file}`: _agrega el archivo {file}_
- `git add .`: _agrega todos los archivos modificados (sin incluir .gitignore)_

### Ejemplo

- **Situación**: Modificamos "README.md" y creamos "nuevo.txt".

**`$ git add .`**

<table>
<tr>
<th>ANTES</th>
<th>DESPUÉS</th>
</tr>
<tr>
<td>

```bash
$ git status
Untracked files:
  nuevo.txt
Changes not staged:
  modified: README.md
```

</td>
<td>

```bash
$ git status
Changes to be committed:
  new file: nuevo.txt
  modified: README.md
```

</td>
</tr>
</table>
