# 11 Deshacer el ultimo commit (perdiendo los cambios realizados en el working copy)

`git reset --hard HEAD^`

Para mover el HEAD al commit anterior al que está apuntando en este momento (HEAD^).

Con el parametro --hard para perder los cambios.

# 12 Rehacer el ultimo commit (el que acabamos de deshacer)

`git reflog`

Para identificar el commit que acabamos de deshacer.

`git reset HEAD@{1}`

Para mover el HEAD al commit especificado.

# 13 Hacer uns merge con 'master' (styled absorbe a master)

No ha causado conflicto. 

master ya forma parte de la historia de styled.

# 19 Hacer un merge de htmlify en styled (styled absorbe a htmlfy)

Si ha causado conflicto.

htmlfy y styled están modificando las mismas lineas del mismo fichero.

# 21 Desde master hacer un merge con styled

No ha causado conflicto.

master está incluido en la historia de styled.

# 25 Dibujar el diagrama

`git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative`

```
*   204c86c - (HEAD -> master, styled) Merge branch 'htmlify' into styled (4 minutes ago) <Sergio Alonso>
|\
| * 7f928a5 - (htmlify) Add html tags (6 minutes ago) <Sergio Alonso>
* | f9d76fa - Add style (34 minutes ago) <Sergio Alonso>
|/
* 1c11fb2 - Add git-nuestro markdown file (36 minutes ago) <Sergio Alonso>
```

# 26 Hacer un merge no fast-forward de title en marter (master absorbe a title)

Si podría ser fast forward.

Porque en master no se ha metido ningun commit nuevo, la rama title parte del ultimo commit de master.

# 27 Deshacer el merge (sin perder los cambios del working copy)

`git reset --soft HEAD^`

# 28 Descartar los cambios

`git reset HEAD git-nuestro.md`

`git checkout -- git-nuestro.md`

# 29 Eliminar la rama title

`git branch -D title`

# 30 Rehacer el merge que hemos desecho

`git reflog`

`git reset --hard 646782e`

# 32 Volver al commit inicial cuando se creó el poema

`git checkout 1c11fb2`

# 33 volver al estado final, cuando pusimos titulo al poema

`git checkout master`



