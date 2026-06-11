## git diff

Muestra las diferencias entre las versiones de los archivos modificados.

### Manual

- `git diff`: _cambios en el working directory (sin stagear)_
- `git diff --staged`: _cambios dentro del staging area_
- `git diff {rama1} {rama2}`: _diferencias entre dos ramas_
- `git diff {hash1} {hash2}`: _diferencias entre dos commits_

### Ejemplo

- **Situación**: Agregamos una línea a "config.txt" pero todavía no hicimos add.

**`git diff` vs `git diff --staged`**

<table>
<tr>
<th>SIN --staged (working dir)</th>
<th>CON --staged (staging area)</th>
</tr>
<tr>
<td>

```bash
$ git diff
diff --git a/config.txt b/config.txt
@@ -1,3 +1,4 @@
 host=localhost
 port=8080
 debug=false
+timeout=30
```

</td>
<td>

```bash
$ git diff --staged
(sin output)
```

</td>
</tr>
</table>

> Una vez hecho `git add`, `git diff` no muestra ningun cambio —
> el cambio está en staging y necesitás `--staged` para verlo.
