# El Caso Práctico · Vive Energía

Juego web de decisiones para practicar el Protocolo de violencia laboral, acoso y hostigamiento (VE-5-PR-04) y el Código de Ética de Vive Energía.

- **Tres recorridos:** Evaluador, Evaluado y módulo del Código de Ética (13 decisiones cada uno).
- **Calificación de 1 a 10** al finalizar y el asistente informativo **Aerojandro**.
- **Acuse de recibo:** al terminar cualquier recorrido, sin importar la calificación, la pantalla final abre `acuse.html` en una pestaña nueva. Es un formulario con el mismo formato del acuse en PDF: casillas "Recibí y leí", campos para escribir con el teclado y firma dibujada con el ratón o con el dedo. El botón "Imprimir / Guardar como PDF" abre el cuadro de impresión del navegador (hoja carta, una sola página).

## Archivos que se suben a GitHub

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | El juego completo (HTML, CSS y JavaScript en un solo archivo). |
| `acuse.html` | Formulario del acuse de recibo. Debe estar en la misma carpeta que `index.html` y conservar ese nombre exacto (GitHub distingue mayúsculas y minúsculas). |
| `README.md` | Esta descripción (opcional). |

No hace falta subir la carpeta `versiones/` (versiones anteriores y los PDF del acuse); Git ya guarda el historial. No hay librerías externas ni carpetas adicionales.

## Cómo viaja la calificación

El juego abre `acuse.html#nota=8`. La parte después de `#` no se envía a ningún servidor; la página la lee en el navegador y escribe "8 / 10" en el campo "Resultado". Si alguien abre `acuse.html` directamente, ese campo queda vacío para escribirlo.

## Publicar en GitHub Pages

1. Sube `index.html` y `acuse.html` a la raíz del repositorio (o de la carpeta que se publicará).
2. En **Settings → Pages**, elige la rama (`main`) y la carpeta (`/ (root)`).
3. El juego quedará en `https://<usuario>.github.io/<repositorio>/`. Los enlaces son relativos y funcionan en cualquier ruta. También funciona abriendo `index.html` como archivo local.

## Probarlo en local

```bash
python -m http.server 8000
```

Abre `http://localhost:8000/index.html`.

## Antes de publicar

- **Privacidad:** el juego resume contenido interno de Vive Energía (políticas, códigos de documentos y datos de contacto). Los documentos fuente indican que no deben divulgarse a terceros sin autorización. GitHub Pages en cuenta gratuita exige repositorio público; para uno privado se necesita un plan de pago. Confirma con Recursos Humanos y Jurídico. Las páginas incluyen `noindex` para que los buscadores no las indexen, pero eso no las protege.
- **Datos personales y firma:** nada se envía a un servidor; el acuse se llena, firma e imprime en el dispositivo de la persona. Quien lo llena es responsable de entregarlo a Recursos Humanos.
- **Validez de la firma:** la firma dibujada en pantalla es una imagen, no una firma electrónica avanzada. Jurídico debe confirmar si es suficiente para el acuse.
- **Impresión:** en el cuadro de impresión conviene elegir "Guardar como PDF" y desactivar "Encabezados y pies de página". El nombre del archivo se sugiere como `Acuse_de_recibo_<nombre>`.
- **Tipografías:** se cargan desde Google Fonts; sin conexión se usa Arial.
- El contenido debe validarlo Recursos Humanos, el Comité o Jurídico antes de difundirse.
