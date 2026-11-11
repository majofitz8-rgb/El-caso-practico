# El Caso Práctico · Vive Energía

Juego web de decisiones para practicar el Protocolo de violencia laboral, acoso y hostigamiento (VE-5-PR-04) y el Código de Ética de Vive Energía.

- **Tres recorridos:** Evaluador, Evaluado y módulo del Código de Ética (13 decisiones cada uno).
- **Calificación de 1 a 10** al finalizar y el asistente informativo **Aerojandro**.
- **Acuse de recibo:** al terminar cualquier recorrido, sin importar la calificación, la pantalla final ofrece descargar `Acuse_de_recibo_politicas.pdf` para firmarlo y entregarlo a Recursos Humanos.

## Archivos

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | El juego completo (HTML, CSS y JavaScript en un solo archivo, sin dependencias ni compilación). |
| `Acuse_de_recibo_politicas.pdf` | Formato de acuse que se descarga al finalizar. **Debe estar en la misma carpeta que `index.html`** y conservar exactamente ese nombre (GitHub distingue mayúsculas y minúsculas). |
| `versiones/` | Versiones anteriores del juego (historial). Puede omitirse al publicar. |

## Publicar en GitHub Pages

1. Sube `index.html` y `Acuse_de_recibo_politicas.pdf` a la raíz del repositorio (o de la carpeta que se publicará).
2. En **Settings → Pages**, elige la rama (`main`) y la carpeta (`/ (root)`).
3. El juego quedará en `https://<usuario>.github.io/<repositorio>/`. Los enlaces son relativos, así que funcionan en cualquier ruta.

## Probarlo en local

```bash
python -m http.server 8000
```

Abre `http://localhost:8000/index.html`.

## Antes de publicar

- **Privacidad:** el juego resume contenido interno de Vive Energía (políticas, códigos de documentos y datos de contacto). Los documentos fuente indican que no deben divulgarse a terceros sin autorización. Usa un **repositorio privado** o confirma con Recursos Humanos y Jurídico que puede ser público. La página incluye `noindex` para que los buscadores no la indexen, pero eso no la protege.
- **Datos personales:** el juego no guarda ni envía datos. El acuse se descarga en blanco y se llena y firma fuera de la página.
- **Tipografías:** se cargan desde Google Fonts; sin conexión se usa Arial.
- El contenido debe validarlo Recursos Humanos, el Comité o Jurídico antes de difundirse.
