# Administrador de Django

Para agregar, editar y borrar los posts que hemos modelado, utilizaremos el administrador de Django.

Vamos a abrir el archivo `blog/admin.py` y reemplazar su contenido con esto:

```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

Como puedes ver, importamos (incluimos) el modelo Post definido en el capítulo anterior. Para hacer nuestro modelo visible en la página del administrador, tenemos que registrar el modelo con `admin.site.register(Post)`.

Ok, es hora de ver tu modelo Post. Recuerda ejecutar `python manage.py runserver` en la consola para correr el servidor web. Ve al navegador y escribe la dirección http://127.0.0.1:8000/admin/. Verás una página de inicio de sesión como la que sigue:

![Página de inicio de sesión](images/login_page2.png)

Para poder entrar deberás crear un *superusuario*, que es un usuario que tiene control sobre todo lo que hay en el sitio. Vuelve a la línea de comandos, escribe `python manage.py createsuperuser` y pulsa intro. Cuando te lo pida, escribe tu nombre de usuario (en minúscula, sin espacios), email y contraseña. No te preocupes si no puedes ver la contraseña mientras la escribes, así es como debe ser. Simplemente escríbela y pulsa `intro` para continuar. La salida de este comando debería verse así (nombre de usuario y dirección de correo electrónico deberían ser los tuyos):

    (myvenv) ~/djangogirls$ python manage.py createsuperuser
    Username: admin
    Email address: admin@admin.com
    Password:
    Password (again):
    Superuser created successfully.

Vuelve al navegador. Inicia sesión con las credenciales de súper usuario que elegiste; deberías ver el panel de administración de Django.

![Administrador de Django](images/django_admin3.png)

Ve a Posts y experimenta un poco con él. Añade cinco o seis entradas de blog. No te preocupes por el contenido, puedes copiar y pegar cualquier texto de este tutorial para ahorrar tiempo :).

Asegúrate que al menos dos o tres entradas (pero no todas) tengan la fecha de publicación. Será de ayuda más tarde.

![Administrador de Django](images/edit_post3.png)

Si quieres saber más sobre el administrador de Django, puedes visitar la documentación de Django: https://docs.djangoproject.com/en/1.9/ref/contrib/admin/

Este probablemente sea un buen momento para tomar un café (o té) o algo para comer y re-energizarte. Creaste tu primer modelo de Django - ¡mereces un pequeño recreo!