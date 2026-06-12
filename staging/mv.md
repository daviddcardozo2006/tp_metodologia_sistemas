git mv
Permite renombrar archivos o moverlos de directorio sin perder el rastro de su historial en Git.

¿Para qué sirve?
En vez de borrar un archivo y crear uno nuevo (lo cual Git interpreta como dos operaciones separadas: delete + add), git mv le avisa a Git que se trata del mismo archivo que cambió de ubicación o nombre. Esto es importante porque git log --follow puede seguir el historial completo de un archivo incluso después de haber sido movido.

Sintaxis
git mv <archivo-origen> <archivo-destino>


Caso de uso real en este repositorio
Durante el desarrollo, el archivo commit.md quedó ubicado en la raíz del proyecto por error, cuando debía estar dentro de commits/. La corrección se hizo así:

git mv commit.md commits/commit.md
git commit -m "fix: move commit.md to commits/ directory"


Resultado en git status:
renamed: commit.md -> commits/commit.md


Diferencia con mover manualmente
Si en cambio se hubiera hecho:
mv commit.md commits/commit.md
git add commits/commit.md
git add commit.md  # marca el original como eliminado

Git también detecta esto como un rename en la mayoría de los casos (gracias a la heurística de similitud de contenido), pero git mv es más explícito y no depende de esa detección automática.

💡 Podés ver el historial completo del archivo, incluso antes de moverse, con:
git log --follow commits/commit.md
