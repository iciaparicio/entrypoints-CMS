# Cómo crear un entrypoint

## Antes de crear un nuevo entrypoint

Es importante que tengas en cuenta que un entrypoint tiene entidad propia, es decir, varias listas de entrypoints pueden contener ese entrypoint. La lógica que hay detrás de este CMS permite mostrar o no el entrypoint en función de la lista a la que pertenezca y de las audiencias para las que esté configurado.

### ¿Qué quiere decir esto exactamente?

Un usuario nunca verá un entrypoint que no le corresponda ver, siempre y cuando ese entrypoint esté correctamente configurado.&#x20;

{% hint style="success" %}
Ejemplo:

_Alice es una usuaria de un dispositivo Android. Alice nunca verá un entrypoint que esté configurado para verse por usuarios solo de iOS._
{% endhint %}

## Crear un entrypoint

Antes de crear o editar un entrypoint asegúrate de estar en la [sección de creación de entrypoints](./#estoy-en-la-seccion-para-crear-o-editar-un-entrypoint).

![Sección para crear entrypoints](.gitbook/assets/seccion\_entrypoints.png)

Haz clic en el botón **Create entrypoint**.

Para cada entrypoint rellena los siguientes campos:

![](.gitbook/assets/entrypoint\_creacion.png)

**Icon default.** Icono asociado al entrypoint, que se muestra cuando los entrypoints se muestran en modo lista. Haz clic en **Set **:outbox\_tray: para añadir un icono.\
:low\_brightness: Es obligatorio.

**Icon dark**. Versión para _dark mode_ del icono asociado al entrypoint. Haz clic en Haz clic en **Set **:outbox\_tray: para añadir un icono.\
:low\_brightness: Es opcional. Si no lo incluyes entonces se usará la versión default también en _dark mode_.

{% hint style="warning" %}
Ten en cuenta que este campo de iconos solo se muestra si la OB lo requiere.&#x20;

* Si no ves este campo en el CMS es que los entrypoints no van acompañados de iconos en ningún caso.
* Si por el contrario tienes este campo visible en el CMS entonces es obligatorio que añadas al menos el **Icon default**.
{% endhint %}

**Entrypoint internal name**. Indica un nombre que describa el entrypoint que estás creando para que luego te resulte más sencillo localizarlo. Este nombre no se muestra a los usuarios.\
:low\_brightness: El nombre puede contener letras tanto mayúsculas como minúsculas, números y espacios pero no admite otros caracteres como guiones bajos, acentos u otros caracteres especiales.

{% hint style="success" %}
:nerd: Cuando indiques el nombre interno piensa de manera natural cómo lo nombrarías para que cualquiera que lo vea entienda qué representa ese entrypoint.&#x20;

_Ejemplo:_

__:thumbsup:_ Programar cita en tienda_\
__:thumbsdown:_ ProgramarCitaTiendaV1_
{% endhint %}

**Entrypoint display name**. Nombre del entrypoint que se ve en la app. Este nombre **sí **lo ve el usuario.

**Entrypoint ID**. Se construye de manera automática en base al Entrypoint internal name pero puedes modificarlo si lo necesitas.

![](.gitbook/assets/crear\_entrypoint\_ID\_automatico.gif)

#### **Carousel images**

Despliega esta sección para añadir las imágenes del entrypoint que estás creando. Son las imágenes que se muestran cuando la lista se configura para mostrarse en modo carrusel.\
:low\_brightness: Estas imágenes no son obligatorias y solo se muestran si en la lista estás configurando el modo de vista Carrusel. Si no incluyes imágenes entonces se verá una imagen con el color base de la OB.

Tienes la opción de incluir dos imágenes:

* Hac clic en **Set image **:outbox\_tray: para añadir la imagen que se mostrará en el carrusel por defecto.&#x20;
* Haz clic en **Set dark imagen **:outbox\_tray: para añadir la imagen que se mostrará en el carrousel en modo noche o _dark mode_.\
  :low\_brightness: Si no la incluyes entonces se mostrará la imagen que incluyas para el modo por defecto.

![](.gitbook/assets/carousel\_images.png)

{% hint style="info" %}
:nerd: Recuerda que la imagen requerida es la de **Set imagen**, a la izquierda. Si solo incluyes la Dark image entonces te pedirá incluir también la Imagen Default.
{% endhint %}

#### **Tracking data**

Información relacionada con el tracking del entrypoint. Con la suma de estos campos se compone la URL de tracking del entry point.\
:low\_brightness: Todos los campos son opcionales

**Category (optional)**. Categoría del entrypoint.

**Action (optional)**. Acción asociada al entrypoint.

**Label (optional)**. Etiqueta que identifica al entrypoint.

![](.gitbook/assets/tracking\_data.png)

### Create your first URL

Configura esta sección para indicar a qué URL lleva el entrypoint cuando el usuario haga clic.

**Add URL**. Selecciona una de las opciones:

* **Preconfigured**. Selecciona esta opción para seleccionar una URL fija, ya preconfigurada. Haz clic en Preconfigured URL data para seleccionar una URL de las disponibles. Cuando lo hagas, puedes consultar (aunque no editar) la **URL** y el provider, que se muestra en el campo **For**.&#x20;
* **Custom**. Selecciona esta opción para añadir una URL a mano.

![Ejemplo de Preconfigured URL y de Custom URL](.gitbook/assets/AddURL\_Entrypoints.png)

Haz clic de nuevo en el desplegable Add URL (optional) y selecciona  para añadir URLs en función de las audiencias.

#### Orden de las URLs

Si añades más de una URL ten en cuenta que el orden en que aparezcan es importante. Es posible que las audiencias sean exclusivas, es decir, que cada entrypoint vaya a una audiencia que no comparta usuarios a los que aplicaría. En ese caso, el orden no es importante.

Pero, ¿qué pasa si las URLs llevan audiencias no exclusivas? Es decir, hay usuarios que pueden cumplir las características de más de una audiencia al mismo tiempo. En este caso, el orden sí importa.&#x20;

El sistema lo que hace es leer de arriba hacia abajo, es decir, mostrará al usuario la URL que primero encuentre buscando desde arriba.&#x20;

Una vez que configures todas las URLs podrás ordenarlas mediante _drag\&drop_.

{% hint style="success" %}
Ejemplo:

🥇Has configurado una URL para la audiencia `los-amantes-del-deporte`. Esta URL lleva a una promo sobre unos nuevos canales de deporte.

🏀Configuras una segunda URL para la audiencia `los-amantes-del-baloncesto`. En este caso la URL lleva a la promo de una serie de documentales sobre la NBA.

_Alice es una usuaria que adora el deporte y por la configuración de las audiencias esta usuaria está integrada dentro de la audiencia `los-amantes-del-deporte` y también en la audiencia `los-amantes-del-baloncesto.`_

¿Qué promo verá Alice? Pues depende del orden en el que coloques las URLs:

Verá la promo de los canales de deporte si colocas las URLs así:

1. `los-amantes-del-deporte`
2. `los-amantes-del-baloncesto`



Verá la promo sobre los documentales de la NBA si colocas las URLs así:

1. `los-amantes-del-baloncesto`
2. `los-amantes-del-deporte`


{% endhint %}

Tienes una URL configurada para la audiencia `los-amantes-del-deporte`

Tienes otra URL configurada para la audiencia `los-amantes-del-baloncesto`

Alice es una usuaria que adora el deporte y por la configuración de las audiencias esta usuaria está integrada dentro de la audiencia `los-amantes-del-deporte` y también en la audiencia `los-amantes-del-baloncesto.`

Se ha configurado una URL sobre un partido de baloncesto súper importante y otra URL sobre nuevos canales de deporte.

#### Cómo borrar una URL

Haz clic en ![](.gitbook/assets/icono\_borrar.png) para eliminar una URL configurada.

Haz clic en el botón **Save and publish** para publicar los cambios.&#x20;

Haz clic en el botón **Save draft** para guardar los cambios sin publicarlos. Podrás publicarlos en otro momento, si lo necesitas.

## Editar un entrypoint

Haz clic en la fila del entrypoint que quieras editar. Se abre la ventana de creación/edición del entrypoint. Haz los cambios que necesites.

{% hint style="warning" %}
Recuerda que hay dos campos que no puedes editar: el **Internal name** y el **ID**
{% endhint %}

Cuando hagas cambios podrás:

* Guardar los campos pero no publicarlos: clic en** Save and unpublish.**
* Guardar los cambios y publicarlos: haz clic en **Save and publish**.
* Iniciar un test: haz clic en **Save and test**
