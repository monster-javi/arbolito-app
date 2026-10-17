# 🌳 Arbolito App

Árbol genealógico con tarjetas y líneas, que se ordena solo. Cargás a la familia, marcás quién es pareja, hijo o hermano de quién, y la app arma el árbol prolijo, generación por generación.

**👉 Usala acá: [monster-javi.github.io/arbolito-app](https://monster-javi.github.io/arbolito-app/)**

---

## Qué hace

**🧩 Tarjetas y vínculos**
- Cada persona es una tarjeta con nombre, fechas, lugar de nacimiento, foto y una nota.
- Las uniones se hacen arrastrando de un punto al otro, o desde la misma tarjeta: agregar padre, madre, pareja, hijo o hermano.
- Al sumar un hijo, la app pregunta si la pareja también es su padre o madre, y le pone el apellido.
- Clic derecho (o mantener apretado en el celu) para crear un hombre o una mujer ahí mismo, y otras acciones rápidas.

**🪄 Reorganizar**
- Ubica a cada generación en su fila y centra a los hijos debajo de sus padres.
- Las parejas quedan siempre juntas, sin nadie en el medio. Los hermanos van para un lado y las parejas para el otro.
- Si alguien tuvo más de una pareja, quedan en cascada para el mismo lado y los hijos de cada pareja debajo de la suya, sin pisarse.
- Los medios hermanos quedan juntos, y la familia de un consuegro puede ubicarse entre dos hermanos si así el árbol queda más limpio.
- **Alinear** endereza las filas sin desarmar lo que acomodaste a mano.

**👨‍👩‍👧 Familias**
- Cada pareja con sus hijos se puede contraer en un bloque “Familia Apellido Apellido”, y se guarda así.
- **Familias −** contrae una generación por vez, de abajo hacia arriba; **Familias +** las vuelve a abrir desde arriba.

**🔎 Y además**
- Búsqueda de personas, deshacer y rehacer, y zoom con ajuste a la pantalla.
- Estilo: tema claro u oscuro, líneas rectas o curvas, y mostrar u ocultar etiquetas, recuadros y leyenda.
- Exportar e importar el árbol en JSON, y copiar y pegar partes entre árboles.
- Español / inglés.
- Funciona en el celular.

## Cuenta y privacidad

- Con tu cuenta, el árbol se guarda en la nube y se sincroniza en vivo entre la compu y el celular. También se puede entrar como invitado.
- Cada usuario ve solo sus datos: la base (Supabase) los protege con Row Level Security.
- **Cifrado de extremo a extremo** opcional, desde Configuración: el árbol y las fotos se guardan cifrados y ni el servidor puede leerlos. El backup también sale cifrado. La contraseña nunca sale de tu navegador; si la perdés, no hay forma de recuperar los datos.
- La clave pública de Supabase que aparece en el código es pública por diseño: lo que protege los datos es RLS.

## Cómo está hecha

- **HTML, CSS y JavaScript** en un único `index.html`, sin compilación, publicado en GitHub Pages.
- Motor de orden propio: elige el orden de cada fila para evitar cruces y después ubica a todos con una optimización que centra a cada familia sobre sus hijos.
- **Supabase** para el login, la base de datos (`arbolito_kv`) y la sincronización en tiempo real.
- **Web Crypto API** para el cifrado (AES-256-GCM, clave derivada con PBKDF2).

Hermana de [Gastos App](https://github.com/monster-javi/gastos-app) y [Task App](https://github.com/monster-javi/task-app): comparten el diseño y la idea. Todas en [monster-javi.github.io](https://monster-javi.github.io/).
