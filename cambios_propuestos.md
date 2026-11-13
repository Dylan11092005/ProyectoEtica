A continuación se presenta el análisis de la estructura actual del proyecto (alojado en el repositorio `Dylan11092005/ProyectoEtica` y desplegado en `proyectortica.vercel.app`), contrastado detalladamente con los requerimientos, correcciones y sugerencias obtenidos en la reunión con **Mariano López Elizondo** (representante y guía del monumento).

---

## 1. Análisis del Estado Actual del Proyecto (Repositorio y Prototipo)

### Estructura del Repositorio
* **Archivos en la raíz (`main`):**
  * `index.html`: Archivo principal (Single Page Application / multipágina simulada por pestañas o secciones dinámicas).
  * `hola.html`: Archivo secundario de prueba.
  * `LEEME-ADMIN.txt`: Documentación o notas administrativas.
  * `img/`: Directorio de recursos gráficos locales.
  * `.gitattributes`: Configuración de Git.
* **Despliegue actual:** `https://proyectortica.vercel.app`.

### Secciones y Elementos Actuales en la Interfaz (`index.html`)
1. **Header y Navegación:**
   * **Nombre actual:** *"Crónica Farallón"* (subtítulo: *"Archivo Mesoamericano"*).
   * **Menú:** `Inicio`, `Actualidad arqueológica`, `Petroglifos y simbología`, `Historia Corobicí`, `Expediciones y rutas`, `Archivo histórico`.
   * **Botones:** CTA *"Visitar monumento"* y selector de tema (Modo Oscuro / Modo Claro).
   * **Cintillo informativo (Ticker/Banner):** Menciona datos académicos genéricos (*"Fotogrametría: más de 40 glifos inéditos..."*).
2. **Sección Inicio (Hero + Resumen):**
   * **Hero:** Título tipo artículo académico (*"El lienzo secreto del río Corobicí..."*), botones *"Leer investigaciones"* y *"Reservar visita"*.
   * **Contadores (KPIs):** `164 Figuras`, `800 Años`, `20 m Muro` (datos de prueba).
   * **Subsección "Investigaciones y ensayos":** 3 tarjetas con autores ficticios.
   * **Subsección "Decodificador de glifos":** Selector interactivo con 4 glifos de prueba (*La Espiral del Agua, El Chamán Alado, La Garra del Felino Solar, Solsticio de Ceniza*) que muestra imagen, descripción extensa y metadatos técnicos.
   * **Subsección "El monumento en imágenes":** Video embebido de YouTube del Banco Central de Costa Rica / Museos BCCR (*"El Farallón de Sandillal: Arte rupestre en Guanacaste"*).
   * **Subsección Boletín:** Formulario para suscribirse a *"El Eco de la Piedra"*.
3. **Sección Actualidad Arqueológica / Archivo Histórico:**
   * Grilla de artículos/ensayos con buscador y filtro por categorías (*Etnohistoria, Conservación, Epigrafía, Arqueología*).
4. **Sección Petroglifos y Simbología:**
   * Vista dedicada al decodificador de glifos.
5. **Sección Historia Corobicí:**
   * Breve reseña (*"Pueblo de los ríos"*) y cronología histórica.
6. **Sección Expediciones y Rutas (y Reservas):**
   * **Tarjetas de actividades:** *Ruta ecuestre*, *Ruta sobre ruedas*, *Caminata por el sendero*, *Ruta de apicultura*.
   * **Tarjetas informativas:** *Horarios* (actualmente dice Lunes a Sábado 8:00–16:00, Domingos 9:00–14:00), *Senderos del Cañón Sandillal*, *Código de respeto*.
   * **Mapa:** Mapa interactivo (OpenStreetMap/Leaflet) con marcador de ubicación.
   * **Formulario de Reserva:** Campos de Nombre, Correo, Fecha y Personas (envío simulado/correo).

---

## 2. Contraste: Estado Actual vs. Requerimientos de la Reunión

| Aspecto / Sección | Estado Actual en el Prototipo | Lo acordado / corregido en la Reunión | Acción Requerida |
| :--- | :--- | :--- | :--- |
| **Nombre Oficial e Identidad** | *"Crónica Farallón - Archivo Mesoamericano"* | **Monumento Arqueológico Nacional El Farallón** (Patrimonio Arquitectónico de la Humanidad desde 1998). | Cambiar el título principal, `<title>`, encabezados y textos legales al nombre oficial. |
| **Logotipo y Paleta de Colores** | Sin logo oficial. Tonos tierra/sepia en modo oscuro y crema en modo claro. | Tienen un **logotipo oficial** cuyos colores son **blanco y dorado**. | Integrar el logo en el Navbar/Footer y ajustar los acentos de la paleta (especialmente el dorado `#D4AF37` o similar y blanco) manteniendo la legibilidad en ambos temas. |
| **Enfoque del Sitio** | Muy académico/revista científica (*boletín para investigadores*). | Enfoque **turístico, cultural y familiar**, diseñado para **causar intriga** e invitar a visitar el sitio físicamente. | Cambiar textos académicos ficticios por información real, atractiva y orientada al visitante. |
| **Decodificador de Glifos (Petroglifos)** | Muestra 4 glifos ficticios con toda la explicación técnica detallada. | Mostrar solo **3 figuras reales** (1 foto grande principal y 3 miniaturas abajo) con una **breve explicación que deje intriga**: *"Si quieres conocer más y saber qué simbolizan ellas, ven y conoce"*. | Rediseñar el componente de petroglifos con estructura de 1 vista principal + 3 miniaturas y un CTA directo a reservar la visita. |
| **Pueblo Indígena** | Menciona *"Corobicí"* de forma general. | Indígenas **Corobicíes** (escrito *"los corobicíes"*), **descendientes de los Chibchas**. | Actualizar la sección de *Historia Corobicí* con este dato etnohistórico exacto. |
| **Actualidad y Prensa** | Ensayos ficticios de doctores inventados. | Noticias y reportajes reales: **Museo del Jade** (dedicatoria), **La Voz de Guanacaste**, **Informe 11** (2 videos), **Más que Noticias**, **Trivisión** (nuevo documental), video de creador mexicano y profesor sancarleño. | Reemplazar tarjetas ficticias por enlaces/embeds reales a estos reportajes y videos. |
| **Horarios de Atención** | Lunes a sábado 8:00–16:00, Domingos 9:00–14:00. | **Lunes a lunes de 6:00 a.m. a 5:00 p.m.** Nota importante: *Se recomienda llegar a más tardar a las 3:00 p.m. para el último tour y aprovechar la luz del día para ver las figuras y tomar fotos*. | Actualizar la tarjeta de horarios con el horario real y la advertencia destacada de las 3:00 p.m. |
| **Duración y Capacidad del Tour** | No especificado / genérico. | Duración: **1.5 a 2 horas**. Mínimo: **1 persona**. Máximo por grupo en el sitio: **12 personas** (pueden llegar 150-200 al lugar, pero bajan en grupos de 12 con guía). | Añadir ficha técnica del tour en la sección de expediciones y reservas. |
| **Tarifas y Precios** | No existen en la web actual. | • **Niños (< 12 años):** Gratis.<br>• **Estudiantes de colegio:** ₡3.000.<br>• **Estudiantes universitarios:** ₡4.500 (negociable).<br>• **Nacionales (Público general):** ₡6.000.<br>• **Extranjeros:** ₡10.000.<br>• **Parqueo:** Gratis. | Crear una sección/tabla de **Tarifas y Beneficios** clara y visible antes de reservar. |
| **Sistema de Reservas** | Formulario estático (Nombre, Correo, Fecha, Personas). | Atención **preferiblemente con reserva previa** (aunque reciben sin reserva) gestionada directamente por **WhatsApp** (atendido por la familia). | Conectar el formulario para que arme un mensaje prellenado hacia la API de WhatsApp (`wa.me/506...`) y añadir botón flotante de WhatsApp. |
| **Rutas y Servicios Adicionales** | Caballo, Bicicleta, Caminata, Apicultura. | Tienen caminata guiada (sombra y acceso al río para bañarse), **2 caballos** para iniciar, y **venta de miel de abeja por temporada**. | Ajustar las tarjetas de actividades para reflejar la realidad (sendero guiado, baño en el río, paseo a caballo inicial y miel por temporada). |
| **Reglas y Recomendaciones** | Código de respeto básico. | • **Permitido llevar alimentos** (agua, refrescos, comida).<br>• **Regla estricta:** Traer su basura de regreso.<br>• **Recomendaciones (verano):** Tenis, repelente, agua, sombrero/gorra, bloqueador solar y pantaloneta (si desean bañarse en el río). | Actualizar la tarjeta de *"Código de respeto y Recomendaciones"* con esta lista detallada. |
| **Responsabilidad Ambiental** | No existe. | Recibieron el galardón de **Bandera Azul Ecológica con 3 estrellas** y llevan **más de 25 años reciclando**. | Crear un bloque/insignia destacada de **Sostenibilidad y Bandera Azul (3 estrellas)**. |
| **Diseño Responsivo (Móvil)** | Tony menciona en la reunión que aún no está adaptado a móviles. | Los clientes y el propio Mariano acceden desde el celular. | Garantizar CSS **100% Mobile-First / Responsivo** (menú hamburguesa, grillas adaptables). |

---

## 3. Elementos Nuevos y Placeholders (Previo a la Gira de Campo)

Dado que el equipo realizará una gira un domingo por la mañana para vivir la experiencia y recolectar material propio, la arquitectura web debe dejar **listos y maquetados** los siguientes apartados con *placeholders* claramente identificados en el código:

### A. Placeholders de Contenido que les enviará Mariano por WhatsApp
1. **Logo Oficial (`[PLACEHOLDER_LOGO]`):** Espacio en el Navbar y Footer preparado para imagen PNG/SVG con estética blanco y dorado.
2. **Historia de la Familia (`[PLACEHOLDER_HISTORIA_FAMILIA]`):**
   * Nueva sección **"Sobre Nosotros / Guardianes del Farallón"**.
   * Datos ya confirmados para el texto base: Familia local que ha protegido y guiado el sitio por más de **30 años** (desde ~1996/1997), incluyendo a los **dos tíos adultos mayores** que viven ahí desde hace más de **50 años** y también imparten el tour. Queda pendiente la "pinceladita" escrita por Mariano y una foto familiar.
3. **Enlaces a Videos y Reportajes (`[PLACEHOLDER_MEDIA_LINKS]`):**
   * Tarjetas listas para insertar las URLs exactas de *Informe 11* (2 videos), *Más que Noticias*, *Trivisión*, *Museo del Jade*, *La Voz de Guanacaste*, el video del creador mexicano y el del profesor sancarleño.
4. **Número de WhatsApp Oficial (`[PLACEHOLDER_WHATSAPP]`):** Variable centralizada en JavaScript para actualizar el número de teléfono en un solo lugar y que funcione tanto en el botón flotante como en el formulario de reservas.

### B. Placeholders que se completarán tras la Visita del Equipo al Sitio
1. **Galería de Atardeceres y Paisajes (`[PLACEHOLDER_ATARDECERES]`):**
   * Mariano sugirió incluir **2 o 3 fotos de atardeceres** en la finca. Se dejará el carrusel/grilla listo con imágenes temporales.
2. **Las 3 Figuras Clave de Petroglifos (`[PLACEHOLDER_3_GLIFOS]`):**
   * Maquetación de 1 imagen grande + 3 miniaturas seleccionables con textos breves de intriga, listas para reemplazar con las fotos reales tomadas por los estudiantes en la gira.
3. **Bitácora de Visitantes / Testimonios (`[PLACEHOLDER_BITACORA]`):**
   * Nueva sección **"30 Años de Bitácoras y Testimonios"**.
   * En la gira podrán tomar fotos a las bitácoras físicas históricas donde firman turistas nacionales y extranjeros, y transcribir 3 o 4 reseñas reales.
4. **Crónica de Experiencia Vivencial (`[PLACEHOLDER_EXPERIENCIA_ESTUDIANTES]`):**
   * Mariano enfatizó la importancia de que el texto refleje que *"fueron, se sentaron y vieron la cantidad real de figuras"*. Se dejará un bloque destacado de testimonio/introducción vivencial para actualizar tras la gira.
5. **Métricas Reales en el Hero (`[PLACEHOLDER_KPIS]`):**
   * Reemplazar o validar los contadores actuales (`164 figuras`, `800 años`, `20 m muro`) por datos verificados en sitio o hitos confirmados (`+30 Años de Conservación`, `1998 Patrimonio Nacional`, `3★ Bandera Azul`, `+25 Años Reciclando`).

---

## 4. Plan de Desarrollo (Hoja de Ruta para la Próxima Consulta)

Para que en tu próxima consulta podamos programar y entregar el código completo y actualizado, trabajaremos bajo este plan estructurado en **4 fases de implementación**:

### Fase 1: Refactorización de Diseño, Paleta y Responsividad (CSS)
1. **Paleta Blanco y Dorado + Tierra:** Ajustar las variables CSS (`--accent-gold`, `--text-light`, etc.) para honrar los colores del logo oficial (blanco y dorado) sin perder la esencia arqueológica en modo oscuro y modo claro.
2. **Responsividad Móvil Total:** Implementar `@media queries` completas para celulares y tablets (menú colapsable en móvil, grillas de 1 columna en pantallas pequeñas, textos y botones táctiles).

### Fase 2: Reestructuración de Secciones y Contenido Confirmado (HTML)
1. **Header & Hero:** Cambiar a *"Monumento Arqueológico Nacional El Farallón"*, añadir enlaces a sus redes reales (`@elfarallon_corobici` en Instagram y página *Farallón Corobicí*) y actualizar contadores.
2. **Sección Petroglifos (Intriga):** Reducir a 1 visor principal + 3 miniaturas con textos cortos que inviten a descubrir el significado en el tour presencial.
3. **Sección Historia Corobicí y Familia:** Actualizar información de los *Corobicíes (descendientes de Chibchas)* e integrar la nueva sección de la **Familia Guardiana (+30 años cuidando el sitio y tíos con +50 años en la zona)**.
4. **Sección Sostenibilidad:** Crear el bloque de **Bandera Azul Ecológica (3 Estrellas)** y los **+25 años de reciclaje**.
5. **Sección Prensa y Videos:** Maquetar el reproductor del BCCR junto con las tarjetas para *Museo del Jade, La Voz de Guanacaste, Informe 11, Más que Noticias y Trivisión*.
6. **Sección Expediciones, Tarifas y Recomendaciones:**
   * Actualizar tarjetas de rutas (Sendero guiado por sombra + baño en el río, Paseo a caballo, Miel de abeja por temporada).
   * Añadir **Tabla de Tarifas Oficiales** (Niños <12 gratis, Colegiales ₡3.000, Universitarios ₡4.500 negociable, Nacionales ₡6.000, Extranjeros ₡10.000, Parqueo Gratis).
   * Actualizar **Horarios** (Lunes a lunes 6:00 a.m. – 5:00 p.m., último ingreso recomendado 3:00 p.m.) y **Detalles del Tour** (1.5 a 2 horas, grupos de 1 a 12 personas).
   * Actualizar **Reglas y Recomendaciones** (Permitido ingresar alimentos, llevarse la basura, llevar tenis, repelente, agua, gorra, bloqueador y pantaloneta).
7. **Sección Bitácora de Testimonios:** Crear el apartado visual que muestre la tradición de las bitácoras físicas de 30 años.

### Fase 3: Funcionalidad Interactiva y Reservas por WhatsApp (JavaScript)
1. **Integración de Formulario con WhatsApp:** Hacer que al enviar el formulario de reserva (Nombre, Fecha, Hora estimada, Tipo de visitantes/Cantidad), se genere automáticamente un enlace a WhatsApp con el mensaje estructurado listo para enviar a la familia.
2. **Botón Flotante de WhatsApp:** Añadir un botón fijo en la esquina inferior derecha para consultas rápidas.
3. **Eliminación de Boletín Ficticio:** Sustituir el formulario de boletín académico *"El Eco de la Piedra"* por un llamado a la acción real hacia Instagram y WhatsApp.

### Fase 4: Marcadores de Código (`TODO / PLACEHOLDER`)
* Dejar todos los bloques pendientes de la gira o de los archivos de Mariano claramente comentados en el código (`<!-- [PLACEHOLDER: ...] -->`) para que reemplazarlos tras la visita del domingo les tome solo unos minutos.

---

**¿Cómo proceder en tu siguiente consulta?**
Cuando estés listo, solo indícame si deseas que genere el `index.html` completo con estos cambios aplicados (o si prefieres ir sección por sección), y si ya cuentas con algún dato adicional (como el número de WhatsApp o el archivo del logo) para incluirlo de una vez.