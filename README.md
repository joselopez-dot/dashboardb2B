# EDUQIA · Dashboard comercial B2B

Dashboard estático de una página para GitHub Pages. Incluye **datos ficticios** extraídos del Excel `Eduqia_Reporting_B2B_MASTER (1).xlsx` y permite importar localmente un Excel con **la misma estructura de hojas**.

## Publicación en GitHub (instrucciones para empezar desde cero)

1. En GitHub, crea **un repositorio NUEVO**, por ejemplo `eduqia-dashboard-b2b`. No uses el repositorio del dashboard de captación B2C.
2. Descomprime este ZIP en tu ordenador. Dentro encontrarás `index.html`, `README.md` y las carpetas `assets` y `data`.
3. Entra en el repositorio nuevo, pulsa **Añadir archivo → Subir archivos** y sube **todo el contenido descomprimido**, respetando las carpetas. El archivo `index.html` debe quedar en el nivel principal del repositorio, no dentro de una carpeta adicional.
4. En **Configuración → Páginas**, en «Compilación e implementación», elige **Implementar desde una rama**, selecciona la rama principal (`main` o `principal`, según se muestre) y la carpeta `/(raíz)`. Pulsa **Guardar**.
5. Cuando GitHub termine la publicación, la web estará disponible en una URL parecida a `https://TU-USUARIO.github.io/eduqia-dashboard-b2b/`. Consulta la URL exacta que aparece en Configuración → Páginas.

## Cómo utilizarlo

- Al abrirlo, verás una **demo con datos ficticios** (del Excel facilitado).
- Pulsa **Cargar Excel** y selecciona un `.xlsx` que contenga las pestañas **KPIs, Pipeline, Forecast y Clientes** (también se aceptan los iconos que tiene la plantilla actual).
- Los datos se procesan **solo en el navegador**, sin enviarse a ningún servidor ni a GitHub. Al recargar la página se vuelve a la demo; para compartir los datos reales hay que compartir el Excel por un canal seguro o usar posteriormente una solución privada.
- Filtra el forecast y las oportunidades por línea de negocio. En la tabla puedes buscar, filtrar por estado, abrir una ficha o exportar las filas visibles en CSV.

## Qué hace y qué NO hace

- Presenta exactamente los valores de las pestañas de origen; no genera series de meses ni inventa actividades comerciales.
- Los KPI comparativos (por ejemplo, tasa de cierre) son valores agregados declarados por el Excel, no cálculos a partir de oportunidades individuales.
- Separa el **pipeline bruto declarado en KPIs**, el **pipeline bruto y ponderado por etapas**, y el **forecast ponderado por líneas**. Señala sus diferencias en «Calidad y coherencia del dato».
- La pestaña «Clientes» contiene solo una lista parcial de oportunidades; los totales de la tabla no son el total del pipeline.
- **No** modifica ni sobrescribe el Excel. Solo lee `.xlsx` y permite exportar una tabla filtrada a `.csv`.
- No incorpora el «Informe Cliente» ni la «Cadencia» al panel ejecutivo porque son materiales complementarios, no registros de operaciones individuales.

## Privacidad

El repositorio puede ser público **solo mientras incluya datos ficticios**. El fichero `data/demo.js` y `data/demo.json` quedan accesibles en GitHub y visibles para cualquiera con la URL. **No sustituyas estos archivos por cifras comerciales reales** en un repositorio público. Al cargar un Excel privado mediante el botón, sus datos permanecen en la pestaña local del navegador y no se comparten automáticamente con tu jefa u otros usuarios.

## Estructura

- `index.html`: página del dashboard.
- `assets/styles.css`: estilos y diseño adaptable a móvil.
- `assets/app.js`: indicadores, gráficos, filtros y lector XLSX local (sin dependencias externas).
- `data/demo.js` y `data/demo.json`: muestra ficticia inicial.

## Compatibilidad

Recomendado: Chrome o Edge actualizados. El lector usa el soporte nativo de descompresión del navegador para los archivos `.xlsx` habituales (OOXML comprimido). No admite archivos `.xls` antiguos, `.xlsm` ni libros cifrados.
