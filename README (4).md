# Libranza Segura VR · Simulador de capacitación en seguridad eléctrica

Simulador de realidad virtual (A-Frame/WebXR) que se abre como página web en PC, celular y Meta Quest. No requiere instalar nada.

- **Práctica 1 · Libranza en tablero de 440 V** (5 reglas de oro).
- **Práctica 2 · Cubiertas aislantes en línea energizada** desde camión canastilla, en el poste del transformador.

## Archivos
| Archivo | Para qué es |
|---|---|
| `index.html` | El simulador completo (escenas, prácticas, registro). |
| `aframe-v1.5.0.min.js` | Motor 3D A-Frame 1.5.0 (licencia MIT). Va junto a `index.html` para que la página no dependa de servidores externos. |
| `README.md` | Esta guía. |

Los tres van en la **raíz** del repositorio (no dentro de carpetas).

## 1. Publicar en GitHub Pages (desde el navegador, sin instalar programas)
1. Entra a https://github.com e inicia sesión (o crea una cuenta gratuita).
2. Arriba a la derecha: **+ → New repository**. Nombre: por ejemplo `libranza-segura-vr`. Marca **Public** (Pages gratis requiere repositorio público). Clic en **Create repository**.
3. En el repositorio nuevo: **Add file → Upload files**. Arrastra los 3 archivos (`index.html`, `aframe-v1.5.0.min.js`, `README.md`). Abajo, clic en **Commit changes**.
4. Ve a **Settings** (pestaña de arriba) → en el menú izquierdo, sección *Code and automation*, **Pages**.
5. En *Build and deployment* → *Source*: **Deploy from a branch**. En *Branch* elige **main** y la carpeta **/ (root)**. Clic en **Save**.
6. Espera 1–3 minutos y recarga esa página de Settings → Pages: aparecerá **"Your site is live at https://TU-USUARIO.github.io/libranza-segura-vr/"**. Esa es la dirección del simulador.
7. Ábrela en la computadora para comprobar que carga (aviso de seguridad → identificación → escena).

**Si ya tenías un repositorio con una versión anterior:** entra al repositorio → **Add file → Upload files** → arrastra los archivos nuevos (se reemplazan los que tienen el mismo nombre) → **Commit changes**. En 1–3 minutos se actualiza la página. Si en el visor sigues viendo la versión anterior, recarga la página (o cierra la pestaña y ábrela de nuevo).

> Importante: el historial de capacitaciones se guarda por dirección. Si cambias el nombre del repositorio o la dirección, el historial anterior queda en la dirección vieja. Descarga el CSV antes de cambiarla.

## 2. Abrir en el Meta Quest 2
No hay que instalar ninguna app ni plugin: se usa el navegador del visor.
1. Enciende el visor y conéctalo al **Wi-Fi**.
2. Abre la app **Navegador** (Browser) desde la biblioteca o la barra de apps.
3. En la barra de direcciones escribe `https://TU-USUARIO.github.io/libranza-segura-vr/` y entra. Guárdala en **favoritos** (estrella) para no volver a teclearla.
4. Acepta el aviso de seguridad y llena la identificación con el teclado del visor.
5. Toca el botón **VR** (ícono de gafas, abajo a la derecha de la página). Si el visor pide permiso para entrar a realidad virtual, acéptalo.
6. Para salir de VR: botón Meta (Oculus) del control derecho.

**Controles en el Quest:** gatillo = láser/clic · joystick izquierdo = caminar (en la canastilla: pluma/giro) · joystick derecho = girar (en la canastilla: telescopio) · **B/Y** = subir/bajar del camión · **A/X** = movimiento automático de la canastilla en la práctica 2.

## 3. Transmitir lo que ve el visor (para la presentación)
**A una computadora o proyector (recomendado):**
1. En la computadora abre **Google Chrome** o **Microsoft Edge** y entra a https://www.oculus.com/casting. Inicia sesión con **la misma cuenta de Meta** que tiene el visor.
2. La computadora y el visor deben estar en **la misma red Wi-Fi**.
3. En el visor: botón Meta → menú → **Compartir / Transmitir (Cast)** → elige **Computadora** → **Siguiente**.
4. Un punto rojo arriba a la derecha en el visor indica que está transmitiendo; en el navegador de la computadora aparece la vista. Pon esa ventana en pantalla completa y conéctala al proyector.

**A un celular:** instala la app **Meta Horizon** (la misma con la que configuraste el visor), mismo Wi-Fi y misma cuenta → ícono **Transmitir** → elige el visor → Iniciar.

**A una TV:** desde el mismo menú **Transmitir** del visor se puede elegir una TV con Chromecast integrado en la misma red.

**Consejos para la presentación:**
- Haz un ensayo completo el día anterior, en el mismo lugar y con la misma red.
- Lleva el visor con batería llena (dura ~2 h) y marca el límite de seguridad (Guardian) en el espacio donde vas a presentar.
- Las redes de empresa a veces bloquean la transmisión entre equipos; si no aparece la computadora en el visor, usa un hotspot/router propio para visor y computadora.
- La transmisión agrega un poco de retraso y baja la fluidez del visor; es normal.

## 4. Problemas comunes
- **La página se queda en blanco o muestra un recuadro rojo de error:** toma foto del mensaje. Revisa que `aframe-v1.5.0.min.js` esté en la raíz del repositorio junto a `index.html`.
- **404 / "There isn't a GitHub Pages site here":** espera unos minutos más, revisa que el archivo se llame exactamente `index.html` (minúsculas) y que Pages esté en *main* / *(root)*.
- **No aparece el botón VR en el Quest:** la dirección debe empezar con **https://**; ábrela desde el Navegador del Quest (no desde otra app).
- **Se ve lento en el Quest:** cierra otras pestañas del navegador y reinicia el visor antes de presentar.

## Inicio: aviso de seguridad e identificación
Al abrir el simulador aparecen dos pantallas antes de entrar a la escena:
1. **Aviso de seguridad:** el trabajador debe marcar "He leído y acepto" para continuar. La fecha y hora de aceptación queda en cada registro.
2. **Identificación:** número de empleado / RPE y nombre completo (obligatorios), área y empresa (opcionales). Si el número ya existe en ese equipo, los datos se llenan solos.

En el Quest y en el celular, estas pantallas se llenan en la página normal (antes de tocar el botón de VR), con el teclado del sistema.

**Registro:** cada práctica terminada se guarda con fecha, práctica, tensión, estado, calificación, pasos completados, errores (con el detalle de cada uno), errores graves, ayudas automáticas usadas y tiempo. Los intentos que se reinician o abandonan a medias también se guardan como "Incompleta". El nombre del trabajador aparece en los pizarrones. El botón de abajo a la izquierda (👷 nombre · Cambiar / historial) cambia de trabajador.

**Historial (instructor):** en la pantalla de identificación, el botón 📋 muestra todas las capacitaciones guardadas en ese equipo, con buscador, y permite **descargarlas para Excel (CSV)** o borrarlas.

**Dónde se guarda:** en el navegador del equipo (Quest, celular o PC). Si se borran los datos del navegador, se pierde el historial: descarguen el CSV periódicamente.

### Opcional: juntar los registros de todos los equipos en una hoja de Google
1. Crea una hoja de cálculo de Google → Extensiones → Apps Script, y pega:
```javascript
function doPost(e) {
  const libro = SpreadsheetApp.getActiveSpreadsheet();
  const hoja = libro.getSheetByName('Registros') || libro.insertSheet('Registros');
  const r = JSON.parse(e.postData.contents);
  const cols = ['fechaLocal','rpe','nombre','area','empresa','practica','tension','estado','calificacion','pasos','errores','graves','ayudas','tiempo','detalle','avisoAceptado'];
  if (hoja.getLastRow() === 0) hoja.appendRow(['Fecha','No. empleado / RPE','Nombre','Área','Empresa','Práctica','Tensión','Estado','Calificación','Pasos','Errores','Errores graves','Ayudas','Tiempo','Detalle de errores','Aviso aceptado']);
  hoja.appendRow(cols.map(function (c) { return r[c] === undefined ? '' : r[c]; }));
  return ContentService.createTextOutput('ok');
}
```
2. Implementar → Nueva implementación → tipo **Aplicación web** → Ejecutar como: **yo** → Quién tiene acceso: **Cualquier persona** → copia la URL.
3. En `index.html`, pega esa URL en `const REGISTRO_URL = '';` y sube el archivo. Cada resultado se seguirá guardando en el equipo y además llegará a la hoja.

## Práctica 1 · Libranza en tablero de 440 V (5 reglas de oro)
1. Equiparse con el EPP correcto (hay 2 distractores: guantes de carnaza y reloj metálico)
2. Delimitar el área con conos
3. Corte efectivo (abrir el interruptor principal)
4. Bloqueo y etiquetado (candado + tarjeta)
5. Verificar ausencia de tensión (probar el probador en fuente conocida y medir L1, L2, L3)
6. Puesta a tierra (barra de tierra primero, luego las 3 fases)

Los errores se cuentan; los graves (tocar partes energizadas o sin EPP) disparan un arco eléctrico simulado. Al final se muestra tiempo, errores y calificación.

## Escena de líneas aéreas y camión canastilla
Sobre la misma calle hay una línea de media tensión (6 postes de concreto con cruceta, 3 fases + neutro, retenida, transformador de 75 kVA con cortacircuito fusible) y un camión canastilla operable.

El camión arranca estacionado en la **zona de maniobra**, pegado al poste del transformador (P-3): torreta a ~2 m del poste, cabina hacia el fondo de la calle y canastilla atrás. Desde ahí la canastilla llega a la altura del pecho junto a las **tres fases** (para colocar cubiertas aislantes), al cortacircuito fusible y a las boquillas del transformador.

Cómo se opera el camión:
1. **Manejar (opcional):** clic en una puerta para subir a la cabina. W/S avanza o da reversa, A/D gira el volante (Quest: joystick izquierdo; gafas de celular: botones del tablero). Tiene alarma de reversa y va a máximo ~11 km/h. Para bajar: tecla **F**, botón **B/Y** del Quest o el botón rojo de la puerta del conductor (si el camión va rodando, frena solo y te baja).
2. En el **mando de la base** (costado derecho, parte trasera) baja los estabilizadores.
3. Sube a la **canastilla** por la parte trasera (clic o mirada fija).
4. Mueve la pluma con el panel a tu derecha o con el teclado/joystick.
5. Para bajar: botón **BAJAR**, tecla **F** o botón **B/Y**. Si la pluma no está en reposo, regresa sola por el mismo camino por el que subiste (así no choca) y te baja al llegar. **GUARDAR** hace lo mismo sin bajarte. Cualquier mando cancela el regreso automático.

Interbloqueos: el camión no avanza con estabilizadores abajo ni con la pluma fuera de reposo; no se pueden bajar estabilizadores si estorba un poste u otro objeto; la pluma no se mueve sin estabilizadores; por debajo de 30° no gira ni extiende; el camión, la canastilla y la pluma no atraviesan conductores, postes, autos, árboles, banquetas ni edificios. El panel de la canastilla muestra la altura y la distancia a la fase más cercana; el del tablero, la velocidad y si estás en la zona de maniobra.

## Práctica 2 · Cubiertas aislantes en línea energizada (poste P-3)
El trabajador cubre las tres fases desde la canastilla con **mangueras de línea** y **cubre-aisladores**, de la fase más cercana a la más lejana. El pizarrón y la mesa de EPP están en la banqueta, junto al camión.

1. EPP para línea energizada (6 elementos): casco dieléctrico, guantes dieléctricos de la clase adecuada, protectores de cuero, mangas dieléctricas, arnés de cuerpo completo y ropa ignífuga. Distractores: reloj metálico, cinturón de liniero y guantes de clase insuficiente.
2. Prueba de aire (inflado) a los guantes.
3. Delimitar el área con 4 conos.
4. Bajar los estabilizadores.
5. Aterrizar el camión a la varilla de tierra.
6. Subir a la canastilla y enganchar el arnés al aro de anclaje (sin arnés la pluma no se mueve y cuenta error).
7. Cubrir la fase C (más cercana): 2 mangueras y después el cubre-aislador.
8. Cubrir la fase B (central).
9. Cubrir la fase A (más lejana).
10. Guardar la pluma y bajar.

**Riesgo por movimiento involuntario:** si la canastilla queda a menos de **30 cm** de una parte de fase **sin cubrir**, se dispara el arco eléctrico y cuenta como error grave (la práctica sale "No aprobado"). Las partes ya cubiertas no cuentan. El panel de la canastilla muestra la fase sin cubrir más cercana y su distancia.

**Cómo llegar a cada pieza:**
- **Tecla F (Quest: botón A o X) = movimiento automático.** En la canastilla, durante los pasos de cubrir las fases, F lleva la canastilla sola a la caja amarilla de la siguiente pieza por la ruta segura. **F otra vez la detiene** ahí mismo y **otra F continúa** desde donde se quedó (útil para explicar durante una presentación). Al llegar, solo se hace clic en la pieza. Mover cualquier control también cancela el movimiento. En esos pasos, para bajar de la canastilla se usa el botón BAJAR o la tecla **X**; en el resto del simulador F sigue sirviendo para subir/bajar.
- **Letrero amarillo con instrucciones (arriba del panel de la canastilla):** dice qué control mantener y hasta dónde, por ejemplo "▲ PLUMA hasta 80° · ahora 42° · mantén W". El botón que toca parpadea en amarillo. Al acercarse al punto la pluma va más lento y **se detiene sola exactamente ahí**; luego aparece la siguiente instrucción. Si mueves otro control, el letrero te dice cómo corregir; si te sales mucho de la ruta segura, te pide GUARDAR para empezar de nuevo. Sigue la misma ruta segura del botón automático.
- **Caja amarilla (guía):** marca dónde debe quedar la canastilla para alcanzar la siguiente pieza.
- **Botón ▶ IR A LA SIGUIENTE PIEZA** (panel de la canastilla): mueve la pluma sola por una ruta segura (≥42 cm de cualquier fase sin cubrir y ≥10 cm de cualquier objeto) hasta esa posición. Si la pluma está en otro lado, primero regresa por donde vino. Cualquier mando lo cancela. Requiere el arnés enganchado y el camión en la zona con estabilizadores abajo. El pizarrón cuenta cuántas veces se usó (para que el instructor lo vea).
- Posiciones de trabajo: la fase C y la fase A se cubren completas desde una sola posición; la fase B (arriba del poste) necesita una posición por pieza.
- Al bajar los estabilizadores dentro de la zona amarilla, el camión queda alineado exacto para que las rutas apliquen.

**Otras reglas:** cubrir una fase lejana antes que la cercana es error; el cubre-aislador va después de las 2 mangueras; cada pieza se coloca solo si está al alcance (≈1.35 m del pecho).

**Tensión:** en el pizarrón se elige 13.2, 23 o 34.5 kV; cambia la clase mínima de guantes (clase 2, 3 o 4, según la tensión máxima de uso de ASTM D120) y la placa del poste.

> Los valores de la simulación (30 cm, alcance, orden de colocación, clases de guantes) son de referencia. Valídalos con un instructor y con el procedimiento vigente de CFE antes de usar la práctica con personal.

La tecla **R** reinicia la práctica en la que estás (1 o 2).

## Controles
- **PC:** WASD/flechas para caminar, arrastrar para mirar, clic para usar lo que está en la mira, R para reiniciar.
- **Gafas de celular (Cardboard / VR Box):** mirar fijo 1.5 s un objeto o un aro azul para activarlo o teletransportarse.
- **Meta Quest:** apuntar y gatillo; joystick izquierdo camina, derecho gira 30°.
- **En la cabina:** W/S avanza/reversa · A/D volante · F baja.
- **En la canastilla:** W/S pluma · A/D giro · Q/E telescopio · X (o F fuera de la práctica 2) guarda la pluma y baja · en la práctica 2, F = movimiento automático a la caja amarilla (Quest: A/X). En Quest: joystick izquierdo pluma/giro, derecho telescopio. En gafas de celular: mirar fijo un botón del panel mueve un tramo corto.

## Requisitos
Se abre como página web con HTTPS (GitHub Pages lo da automáticamente). Modo VR: navegador del Meta Quest y Chrome para Android. En PC funciona con teclado y mouse; en iPhone se puede ver pero sin modo VR.
