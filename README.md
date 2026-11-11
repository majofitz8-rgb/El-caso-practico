# El Caso Práctico · Vive Energía

Juego web de decisiones para practicar el Protocolo de violencia laboral, acoso y hostigamiento (VE-5-PR-04) y el Código de Ética de Vive Energía.

- **Tres recorridos:** Evaluador, Evaluado y módulo del Código de Ética (13 decisiones cada uno).
- **Calificación de 1 a 10** al finalizar y el asistente informativo **Aerojandro**.
- **Acuse de recibo:** al terminar cualquier recorrido, sin importar la calificación, la pantalla final muestra un formulario para llenar el acuse (datos, casillas "Recibí y leí" y firma dibujada con el ratón o con el dedo) y descarga el PDF firmado, que se entrega a Recursos Humanos.

## Archivos

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | El juego completo (HTML, CSS y JavaScript en un solo archivo). |
| `Acuse_de_recibo_politicas.pdf` | Formato de acuse **rellenable** (casillas y campos de texto). Es la plantilla que usa el juego y también se puede descargar en blanco. Debe estar junto a `index.html` y conservar ese nombre exacto (GitHub distingue mayúsculas). |
| `lib/pdf-lib.min.js` | Librería [pdf-lib](https://pdf-lib.js.org/) (licencia MIT, ver `lib/LICENSE-pdf-lib.txt`). Se carga solo al generar el acuse y permite llenar el PDF en el navegador, sin servidor. |
| `versiones/` | Versiones anteriores del juego y el PDF original sin campos. Puede omitirse al publicar. |

### Campos del PDF

`nombre`, `empleado`, `puesto`, `area`, `fecha`, `resultado`, `doc1` a `doc6` (casillas de los documentos), `aprobada`, `no_aprobada`, `rh_recibido_por` y `rh_fecha`. La firma se estampa como imagen en la celda "Firma" (x=212, y=128, 328 × 43 puntos PDF, medidos desde la esquina inferior izquierda de la página). Si se cambia el diseño del PDF, hay que ajustar esas coordenadas en `index.html` (función `initAcuse`).

## Publicar en GitHub Pages

1. Sube `index.html`, `Acuse_de_recibo_politicas.pdf` y la carpeta `lib/` a la raíz del repositorio (o de la carpeta que se publicará).
2. En **Settings → Pages**, elige la rama (`main`) y la carpeta (`/ (root)`).
3. El juego quedará en `https://<usuario>.github.io/<repositorio>/`. Los enlaces son relativos y funcionan en cualquier ruta.

> **Importante:** el acuse firmado se genera leyendo el PDF con `fetch`, lo cual requiere abrir la página desde una dirección web (GitHub Pages o un servidor local), no haciendo doble clic en `index.html`. Abierto como archivo local, el juego funciona, pero el botón "Generar acuse firmado" muestra un aviso y solo sirve la descarga del formato en blanco.

## Probarlo en local

```bash
python -m http.server 8000
```

Abre `http://localhost:8000/index.html`.

## Antes de publicar

- **Privacidad:** el juego resume contenido interno de Vive Energía (políticas, códigos de documentos y datos de contacto). Los documentos fuente indican que no deben divulgarse a terceros sin autorización. Usa un **repositorio privado** o confirma con Recursos Humanos y Jurídico que puede ser público. La página incluye `noindex` para que los buscadores no la indexen, pero eso no la protege.
- **Datos personales y firma:** nada se envía a un servidor; el acuse se genera y descarga en el dispositivo de la persona. Quien lo llena es responsable de entregarlo a Recursos Humanos.
- **Validez de la firma:** la firma dibujada en pantalla es una imagen, no una firma electrónica avanzada. Jurídico debe confirmar si es suficiente para el acuse.
- **Tipografías:** se cargan desde Google Fonts; sin conexión se usa Arial.
- El contenido debe validarlo Recursos Humanos, el Comité o Jurídico antes de difundirse.
