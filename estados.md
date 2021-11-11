# Estados

Es importante que conozcas los estados en los que se pueden encontrar las listas y los entrypoints.

### Entrypoints

**DRAFT**. Estado en el que está un entrypoint cuando lo creas por primera vez y guardas los cambios antes de publicar.

**PUBLISHED**. Estado publicado. El usuario verá el entrypoint siempre que esté configurado para una audiencia que le aplique al usuario y dentro de una lista que también esté publicada.&#x20;

{% hint style="warning" %}
Recuerda que un entrypoint puede estar en diferentes listas y para que se vea tiene que estar publicado. Pero el el hecho de que el entrypoint esté en estado **PUBLISHED** no significa que se vaya a ver. Eso depende del estado en que esté la lista o las listas que lo contengan y las audiencias configuradas en esas listas.
{% endhint %}

**PAUSED**. Estado no publicado. El entrypoint ha estado publicado en algún momento pero ya no lo está, no es visible por ningún usuario.

**TEST**. El entrypoint tiene un test en curso.&#x20;

:nerd: Para más información sobre cómo se comporta un test en un entrypoint consulta la sección [Test sobre un entrypoint](como-hacer-un-test.md#test-sobre-un-entrypoint).

Aquí tienes un pequeño esquema de cómo se puede transicionar de un estado a otro.

![Cómo transiciona un entrypoint de un estado a otro en función del estado de inicio ](.gitbook/assets/Estados\_entrypoint.png)

### Listas

**DRAFT**. Estado en el que está una lista cuando lo creas por primera vez y guardar los cambios antes de publicar.

**PUBLISHED**. Estado publicado. El usuario verá la lista y por tanto los entrypoints que le correspondan según las audiencias configuradas.&#x20;

**PAUSED**. Estado no publicado. La lista ha estado publicada en algún momento pero ya no lo está, no es visible para ningún usuario.

**TEST**. La lista puede tener un test en curso. Este estado siempre se combina con:

* **PAUSED + TEST**. En este caso, la lista está bajo un test y mientras está corriendo el test no lo ven los usuarios, solo los configurados para el Test.
* **PUBLISHED + TEST**. En este caso, la lista está bajo un test pero continúa publicada para el resto de usuarios. Los usuarios del test verán la versión test de la lista y el resto de usuarios verán la lista tal y como estaba de inicio, en la versión publicada.

Aquí tienes un pequeño esquema de cómo se puede transicionar de un estado a otro.

![Cómo transiciona una lista de un estado a otro en función del estado de inicio](.gitbook/assets/Estados\_listas.png)

