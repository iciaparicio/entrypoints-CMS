---
description: Prueba el contenido antes de publicarlo con la opción de Test
---

# Cómo hacer un test

Lo ideal es usar la funcionalidad de test que te ofrece la herramienta para que visualices el contenido antes de impactar a una masa amplia de usuarios.

## Cómo probar un contenido antes de publicarlo

El CMS está dividido en dos partes, la configuración de listas de entrypoints y la configuración de los propios entrypoints.

La forma de probar el contenido es prácticamente igual en ambos casos: siempre que se produzcan cambios o al final del proceso de creación de un nuevo elemento entonces se habilita en el CMS la opción de Test.

### Configurar un test

La opción para crear un test se muestra cuando se producen cambios, es decir, cuando hay algo que probar. También se puede hacer un test de un contenido que acabas de crear y cuyo resultado necesitas visualizar antes de impactar a una masa x de usuarios.

#### Test en listas de entrypoints

* Si la lista está en modo borrador se muestra la opción de test al guardar los cambios pero sin publicarlos. Haz clic en **Test** para crear un test sobre esa lista.&#x20;

{% hint style="warning" %}
Ten en cuenta que si creas un test cuando la lista está en modo **DRAFT** entonces la lista pasa automáticamente a estado **PAUSED**.
{% endhint %}

* Si la lista está publicada o pausada se muestra la opción de test cuando hagas cambios sobre esa lista. En ese caso haz clic en **Save and start test** para guardar esos cambios e iniciar un test.&#x20;

En ambos casos indica:

**Test description**: añade una descripción que te ayude a identificar qué estás probando, cuáles son los cambios.

**Novum user IDs (optional)**: añade uno o más user IDs, separados únicamente por comas (sin espacios) en los que quieras hacer las pruebas. Es un campo opcional.

Haz clic en **Create test**.

![](.gitbook/assets/Create\_test.png)

{% hint style="info" %}
**Cómo obtener el user ID**

1. Asegúrate de tener descargada la versión Enterprise de la app.
2. Abre la app
3. Agita el teléfono
4. Accede a la sección "Autentication"
5. el número que necesitas es el del campo **User ID**
{% endhint %}

#### Test en un entrypoint

A diferencia del caso de las listas, no puedes hacer un test sobre un entrypoint que está en modo borrador.&#x20;

En el caso de entrypoints en estado publicado, haz los cambios que necesitas probar y haz clic en la opción de **Save and start test**. Indica:

**Test description**: añade una descripción que te ayude a identificar qué estás probando, cuáles son los cambios.

**Novum user IDs (optional)**: añade uno o más user IDs, separados únicamente por comas (sin espacios) en los que quieras hacer las pruebas. Es un campo opcional.

Haz clic en **Create test**.

![](.gitbook/assets/Create\_test.png)

### Cómo publicar el contenido de un test

Para empezar, sabrás que una lista de entrypoints tiene un test en marcha gracias a la etiqueta de estado **TEST**:

![Detalle de la etiqueta TEST en una lista de entrypoints](.gitbook/assets/detalle\_test\_tag.png)

Para publicar el contenido de un test accede a la lista de entrypoints sobre la que está en marcha ese test.

Al abrir la lista, el contenido aparece dividido en dos pestañas para que puedas ver, en todo momento, el contenido previo al test y el propio contenido del test.

![Detalle de las pestañas de contenido previo y de test](.gitbook/assets/detalle\_pestañas\_test.png)

&#x20;

{% hint style="warning" %}
Solo puedes hacer cambios en el contenido si estás en la pestaña **Test**. Usa la otra pestaña para ver el contenido previo a los cambios que has hecho para el test.&#x20;
{% endhint %}

Cuando te hayas asegurado que el contenido que tienes en la pestaña **Test**, en todos los pasos, es el contenido que quieres aplicar entonces haz clic en **Publish**. Haz clic en **Yes** en el mensaje de confirmación.

![](.gitbook/assets/Detalle\_Publish.png)

Haz clic en **Close** para volver a la pantalla principal de listas de entrypoints, **Entrypoint Lists**.

{% hint style="success" %}
:thumbsup:En la pantalla principal puedes comprobar que en el estado de la lista ha desaparecido la etiqueta **TEST**.
{% endhint %}

### Cómo descartar un test

Si tras probar el contenido de una lista de entrypoints, con un Test en curso, decides descartar los cambios entonces accede a la lista de entrypoints sobre la que está en marcha ese test.

Haz clic en **Continue** hasta llegar al último paso **Preview & Validate** y haz clic en **Delete test**.

![](.gitbook/assets/Detalle\_DeleteTest.png)

Cuando descartas un test implica eliminar los cambios que habías hecho sobre la lista de entrypoints y el contenido se crea como estaba previamente.

### Como añadir, quitar o modificar los Novum user IDs de un test

Si necesitas editar el test para poder añadir, quitar o modificar los usuarios que pueden ver un determinado test entonces accede a esa lista.

En la pestaña **Test** puedes consultar, en el primer paso **Overview**, la información relativa al test: la descripción, quién lo ha iniciado y la fecha de creación.

Haz clic en ![](.gitbook/assets/editar\_icono.png)para modificar los números de usuario. También para añadir user ID nuevos o eliminar lo que ya hay. Haz clic en **Save** para guardar los cambios.

![](.gitbook/assets/Change\_test\_IDs.gif)
