## git log

Muestra el historial de _commits_ del repositorio con su identificador, autor y descripción.

### Manual

- `git log`: _historial completo con metadata_
- `git log --oneline`: _versión resumida con un commit por línea_
- `git log --oneline --graph`: _historial con representación visual de las ramas_
- `git log --author="{nombre}"`: _filtra commits por autor_

### Ejemplo

- **Situación**: Consultamos el historial del repositorio con distintos flags.

**`git log --oneline` vs `git log --oneline --graph`**

<table>
<tr>
<th>SIN --graph</th>
<th>CON --graph</th>
</tr>
<tr>
<td>

```bash
$ git log --oneline
e4f5g6h docs: update index
a3f9c2b feat: add restore doc
7d1e4f2 feat: add status doc
3c8b1a0 feat: add add doc
```

</td>
<td>

```bash
$ git log --oneline --graph
* e4f5g6h docs: update index
*   a3f9c2b Merge branch 'feature/restore'
|\
| * 7d1e4f2 feat: add restore doc
|/
* 3c8b1a0 feat: add add doc
```

</td>
</tr>
</table>

> `--graph` es especialmente útil para visualizar merges y la divergencia entre ramas.
