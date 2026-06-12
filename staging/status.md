## git status

Muestra el estado actual del _working directory_ y el _staging area_: qué archivos fueron modificados, cuáles están listos para el próximo _commit_ y cuáles no estamos rastreando.

### Manual

- `git status`: _muestra el estado completo_
- `git status -s`: _versión concisa (short)_

### Ejemplo

- **Situación**: Tenemos "README.md" recién modificado, "nuevo.txt" sin trackear, y "config.txt" que ya se encuentra en staging.

**`$ git status`**

<table>
<tr>
<th>SALIDA COMPLETA</th>
<th>SALIDA RESUMIDA (-s)</th>
</tr>
<tr>
<td>

```bash
$ git status
On branch main
Changes to be committed:
  modified: config.txt

Changes not staged for commit:
  modified: README.md

Untracked files:
  nuevo.txt
```

</td>
<td>

```bash
$ git status -s
M  config.txt
 M README.md
?? nuevo.txt
```

</td>
</tr>
</table>

> La columna izquierda del `-s` indica el estado en _staging_, la derecha en _working directory_.
> `M` = modificado, `??` = untracked, `A` = nuevo en staging.
