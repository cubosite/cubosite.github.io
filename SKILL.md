# SKILL: Cubosite Manual de Operaciones y Estándares Técnicos 🧊

## 1. Visión General del Proyecto
* **Proyecto:** Cubosite (Bitácora y exploración digital para almacenar películas, videos, reflexiones y noticias).
* **Tecnología Base:** Astro (Static Site Generation - SSG).
* **Despliegue:** GitHub Pages mediante GitHub Actions.
* **Diseño y Estética:** Interfaz minimalista, oscura y multitema con simetría visual absoluta entre la página principal (`index.astro`) y las vistas de detalle (`[slug].astro`).

---

## 2. Categorías Oficiales del Blog
Las publicaciones se organizan estrictamente bajo las siguientes categorías predefinidas en la navegación y filtros:
* **Terror**
* **Comedia**
* **Ficción**
* **Drama**
* **Acción**
* **Suspenso**
* **+Archivos**

---

## 3. Componentes Clave del UI/UX
* **Header Superior (Hero Top Bar):**
  * **Selector de Temas:** Botones interactivos para alternar dinámicamente entre `Dark` (🌙), `Gris Claro` (☀️) y `Green` (🟢), con persistencia en `localStorage`.
  * **Widget de Información Unificado (`.info-widget`):** Contiene de izquierda a derecha:
    1. **Reloj en Vivo:** Formato de 12 horas con AM/PM (sin segundos) actualizándose en tiempo real.
    2. **Clima Dinámico:** Temperatura ambiental real e iconos meteorológicos obtenidos asíncronamente mediante la API de Open-Meteo.
    3. **IP del Usuario:** Dirección IP pública consultada mediante `ipify.org`.
* **Navegación y Búsqueda:**
  * Buscador superior e inferior integrados y sincronizados.
  * Sistema de filtrado por categoría en el `index.astro` y redirección inteligente de búsqueda hacia la página principal desde las vistas de artículos.
* **Paginación:**
  * Límite estricto de **24 publicaciones por página** en el `index.astro` con controles interactivos de avance/retroceso y desplazamiento suave automático.

---

## 4. Reglas Críticas de Desarrollo y Compilación (SSG)
* **Compatibilidad con Node / esbuild en GitHub Actions:**
  * Las consultas dinámicas (Clima, IP) deben ejecutarse **siempre en el cliente mediante scripts `<script>` optimizados**, asegurando bloques limpios y bien cerrados para evitar errores de sintaxis (`Unexpected end of file`) durante la compilación estática.
* **Sincronización Estructural:**
  * Cualquier modificación en el diseño del header, footer o variables globales de diseño (`:root[data-theme="..."]`) debe replicarse de manera simétrica tanto en `src/index.astro` como en `src/pages/posts/[slug].astro`.

---

## 5. Comandos de Operación
1. **Desarrollo Local:** `npm run dev`
2. **Compilación de Prueba:** `npm run build`
3. **Publicación:** Sincronización mediante commits directos al repositorio principal.
