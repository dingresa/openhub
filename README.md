# OpenHub

## Idea principal

**OpenHub** es una plataforma web de minijuegos clásicos, creada por un programador valenciano como proyecto de aprendizaje en programación web.

La idea es ofrecer un selector de minijuegos accesible desde cualquier navegador y dispositivo, siempre que haya conexión a internet, sin instalar nada. Basta con abrir la página, iniciar sesión y jugar.

Es un proyecto **libre y de código abierto**. Todos los juegos están desarrollados por el autor del proyecto, y cualquier persona puede estudiarlos, modificarlos, mejorarlos, corregir errores o proponer cambios mediante *issues* y *pull requests*.

---

## Licencia

- **Código:** [GNU Affero General Public License v3.0 o posterior](https://www.gnu.org/licenses/agpl-3.0.html) (`AGPL-3.0-or-later`). Puedes usar, estudiar, modificar y compartir el código, pero cualquier versión modificada que se ofrezca a través de una red también debe publicar su código fuente bajo la misma licencia.
- **Imágenes y recursos gráficos:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es), salvo que se indique lo contrario.
- **Nombre y logotipo:** el nombre "OpenHub" y su logotipo identifican el proyecto original. Si haces un *fork*, por favor usa un nombre distinto.

El texto completo de la licencia está en el archivo [`LICENSE`](LICENSE).

---

## Estructura general del proyecto

```
📂 openhub/
├── 📄 index.html
├── 📄 css.html
├── 📁 imagenes/
│       ├── 📁 logo/
│       ├── 📁 fondos/
│       ├── 📁 iconos/
│       └── 📁 portadas/
├── 📁 menusjuegos/
│       └── 📄 menu.html
└── 📁 juegos/
        ├── 📄 minijuegos.html
        ├── 📁 snake/
        │       ├── 📄 snake.html
        │       └── 📄 config.js
        ├── 📁 buscaminas/
        │       ├── 📄 buscaminas.html
        │       └── 📄 config.js
        └── 📁 ajedrez/
                ├── 📄 ajedrez.html
                └── 📄 config.js
```

---

## Página de inicio

### Objetivo

- Presentar la página al usuario con una pantalla de inicio de sesión (versión de prueba).
- Aplicar una estética con colores degradados entre morado, azul y negro.

### Explicación de contenidos

- **`index.html`:** es la página principal y la primera que ve el usuario. Contiene el formulario de inicio de sesión, donde se accede con una cuenta personal. Esta cuenta permite proteger los datos del usuario y guardar su progreso en los juegos.
- **`css.html`:** contiene los estilos de la página, es decir, cómo se ve: colores, degradados, tipografías, tamaños y disposición de los elementos. Al estar separado del contenido, cambiar el aspecto de la web no obliga a tocar el resto de archivos.

### Estructuración

```
📂 openhub/
├── 📄 index.html
└── 📄 css.html
```

---

## Página de menú

### Objetivo

- Permitir la selección de minijuegos.
- Ofrecer la configuración de idioma y de perfil.

### Explicación de contenidos

- **`menu.html`:** es la pantalla que aparece tras iniciar sesión. Funciona como un catálogo de juegos en el que cada uno se muestra con:
  - Una **imagen de portada**.
  - Una **breve descripción** de en qué consiste.
  - Un **manual de uso** con los controles y las reglas.
- Desde este menú el usuario también puede **cambiar el idioma** de la página y **editar su perfil** (nombre, datos de la cuenta, etc.).

### Estructuración

```
📂 openhub/
├── 📄 index.html
├── 📄 css.html
└── 📁 menusjuegos/
        └── 📄 menu.html
```

---

## Carpeta de imágenes

### Objetivo

- Reunir en un único lugar todos los recursos gráficos de la página, para mantenerlos ordenados y localizarlos fácilmente.

### Explicación de contenidos

La carpeta `imagenes/` se divide en cuatro subcarpetas según el uso de cada recurso:

- **`logo/`:** el logotipo de OpenHub en distintos formatos y tamaños (por ejemplo, para la cabecera de la página o para la pestaña del navegador).
- **`fondos/`:** imágenes de fondo y texturas que acompañan a los degradados morado, azul y negro.
- **`iconos/`:** iconos pequeños de la interfaz, como los de idioma, perfil, ajustes o cerrar sesión.
- **`portadas/`:** una imagen representativa de cada minijuego (por ejemplo, `snake.png`, `buscaminas.png` y `ajedrez.png`), que se muestra en el menú de selección.

> **Nota para colaboradores:** las imágenes que se añadan al proyecto deben ser propias o tener una licencia compatible con la del repositorio.

### Estructuración

```
📂 openhub/
├── 📄 index.html
├── 📄 css.html
├── 📁 menusjuegos/
│       └── 📄 menu.html
└── 📁 imagenes/
        ├── 📁 logo/
        ├── 📁 fondos/
        ├── 📁 iconos/
        └── 📁 portadas/
```

---

## Carpeta de minijuegos

### Objetivo

- Reunir todos los minijuegos del proyecto. Cada uno tiene su propia carpeta, con su archivo HTML y sus archivos JS o de configuración.

### Explicación de contenidos

- **`minijuegos.html`:** archivo común a todos los juegos. Sirve de punto de conexión entre el menú y cada minijuego.
- **Carpeta de cada juego** (`snake/`, `buscaminas/`, `ajedrez/`...): contiene todo lo necesario para que ese juego funcione de forma independiente:
  - **Archivo HTML** (`snake.html`, `buscaminas.html`...): la estructura visual del juego.
  - **`config.js`:** la programación y los ajustes del juego, como la lógica, las reglas, la dificultad y las puntuaciones. Al estar todo en un mismo lugar, cualquier persona puede abrir la carpeta de un juego, entenderlo y mejorarlo sin afectar al resto.
- Para **añadir un juego nuevo** basta con crear una carpeta con su HTML y su JS, y darlo de alta en el menú.

### Estructuración

```
📂 openhub/
├── 📄 index.html
├── 📄 css.html
├── 📁 imagenes/
├── 📁 menusjuegos/
│       └── 📄 menu.html
└── 📁 juegos/
        ├── 📄 minijuegos.html
        ├── 📁 snake/
        │       ├── 📄 snake.html
        │       └── 📄 config.js
        ├── 📁 buscaminas/
        │       ├── 📄 buscaminas.html
        │       └── 📄 config.js
        └── 📁 ajedrez/
                ├── 📄 ajedrez.html
                └── 📄 config.js
```

---

## Contribuir

Las contribuciones son bienvenidas: corrección de errores, mejoras en los juegos, nuevos minijuegos, traducciones o sugerencias.

1. Haz un *fork* del repositorio.
2. Crea una rama para tu cambio (`git checkout -b mi-mejora`).
3. Guarda tus cambios (`git commit -m "Descripción del cambio"`).
4. Envía tu rama (`git push origin mi-mejora`).
5. Abre un *pull request* explicando qué has cambiado y por qué.

Al enviar código, aceptas que se publique bajo la misma licencia del proyecto (`AGPL-3.0-or-later`).

Para incluir la licencia en tus archivos, añade esta línea al principio de cada archivo de código:

```
// SPDX-License-Identifier: AGPL-3.0-or-later
```

---

## Privacidad y seguridad

- Las cuentas y los datos de guardado de los usuarios **no forman parte del repositorio**.
- No subas nunca contraseñas, claves de acceso ni bases de datos al repositorio.
- Si encuentras un fallo de seguridad, avisa de forma privada al autor antes de hacerlo público.

---

## Autor

Proyecto creado por un programador valenciano, con las ganas de seguir aprendiendo programación web.