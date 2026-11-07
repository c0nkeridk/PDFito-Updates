# PDFito — Actualizaciones oficiales

Este repositorio público contiene **únicamente APK y notas de lanzamiento** de PDFito. El código fuente se mantiene en un repositorio privado distinto.

## Cómo publicar una versión manualmente

1. Compilar el APK en el repositorio privado de PDFito.
2. Descargar el artefacto de GitHub Actions y extraer el archivo `.apk`.
3. **Importante:** para actualizaciones fiables, utilizar un APK firmado con una **clave de firma permanente**, no un APK debug generado con claves distintas en cada ejecución. Guardar la clave en GitHub Actions Secrets del repositorio privado; nunca subirla a este repositorio público.
4. Abrir [New release](https://github.com/c0nkeridk/PDFito-Updates/releases/new).
5. Crear una etiqueta con el formato `v0.3.1` (o la versión que corresponda a la aplicación).
6. Adjuntar el APK firmado como archivo de la versión; escribir los cambios y publicar como versión **estable** (no draft ni prerelease).
7. En la aplicación PDFito, abrir el engrane y seleccionar **Comprobar actualizaciones**. Si la versión publicada es mayor que la instalada, la app ofrecerá abrir la descarga.

**Estado actual:** todavía falta configurar la firma persistente y publicar el primer APK. Hasta entonces, el botón de actualización de PDFito no encontrará ninguna versión.

La instalación siempre requiere confirmación del usuario en Android. Las actualizaciones deben usar el mismo identificador de aplicación y la misma clave de firma que la versión instalada. La primera migración desde un APK debug puede requerir una reinstalación si las firmas no coinciden; antes de hacerlo, respaldar los documentos y tener en cuenta que se podrían perder los datos locales de la aplicación.
