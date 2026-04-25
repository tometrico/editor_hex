# editor_hex
Editor hexadecimal diseñado en javascript
# Matrix Binary Suite v7.0 - Editor Hexadecimal Profesional

![Version](https://img.shields.io/badge/version-7.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)

## 📋 Descripción General

**Matrix Binary Suite** es un editor hexadecimal avanzado que permite visualizar, editar y analizar archivos a nivel de bytes. Desarrollado completamente en HTML5, CSS3 y JavaScript puro, funciona directamente en el navegador sin necesidad de instalación ni servidor.

### 🎯 Características Principales

- **Editor Hexadecimal interactivo** con edición directa por teclado
- **Soporte para múltiples formatos** (hexadecimal, binario y decimal)
- **Vista previa de imágenes** en tiempo real (BMP, JPEG, PNG, GIF)
- **Búsqueda avanzada** (texto y patrones hexadecimales)
- **Análisis de metadatos** y propiedades del archivo
- **Clonación de fragmentos** y edición por lotes
- **Mapeo de píxeles a bytes** (para imágenes BMP)
- **Interfaz redimensionable** con panel lateral ajustable

---

## 🚀 Instalación y Uso

### Instalación
```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/matrix-binary-suite.git

# Abrir el archivo en el navegador
cd matrix-binary-suite
open index.html


Uso Básico
Cargar un archivo: Archivo → Abrir Archivo...

Activar edición: Haz clic en ⚡ LIVE: OFF para cambiar a ON

Navegar: Usa las teclas de flecha (← → ↑ ↓) para moverte

Editar bytes: Selecciona un byte y escribe directamente (0-9, A-F)

Guardar cambios: Archivo → Guardar Cambios (Exportar)


Opción	Descripción
Abrir Archivo	Carga cualquier archivo (hasta tamaño limitado por memoria)
Guardar Cambios	Exporta el archivo con todas las modificaciones aplicadas
🔍 Búsqueda
Opción	Descripción
Texto (Ignorar Mayúsculas)	Busca cadenas de texto sin distinción
Texto (Exacta)	Búsqueda sensible a mayúsculas
Hexadecimal	Busca patrones HEX (ej: 42 4D)
Ir a Offset	Navega directamente a una posición decimal
🛠️ Herramientas
Opción	Descripción
Estadísticas	Muestra entropía, nulobytes y ediciones
Clonar Fragmento	Copia un rango de bytes a otra ubicación
Limpiar Ediciones	Restaura el archivo original
Propiedades	Información del sistema del archivo
Metadatos	Extrae EXIF y propiedades EMBEBIDAS
🎨 Formato
Opción	Visualización
Hexadecimal	2 dígitos HEX (ej: FF, 1A)
Binario	8 bits (ej: 11111111)
Decimal	0-255 (ej: 255)
🖼️ Soporte para Imágenes
Formatos Soportados
BMP (incluye mapeo de píxeles a bytes)

JPEG / JPG

PNG

GIF

Características
Vista previa en tiempo real al editar bytes

Clic en la imagen → Salta al byte correspondiente

Actualización automática al modificar datos

Redimensionamiento dinámico del panel

🧮 Metadatos Extraídos
Metadato	Descripción
Nombre archivo	Nombre original del archivo
Tipo MIME	Tipo de contenido detectado
Tamaño	En KB y bytes
Magic bytes	Cabecera del archivo (primeros 8 bytes)
Formato detectado	JPEG, PNG, GIF, BMP, etc.
Dimensiones	Ancho y alto (para imágenes)
Entropía	Aleatoriedad de los datos (bits/byte)
Valores únicos	Cantidad de bytes distintos
📊 Estadísticas Disponibles
Nulobytes: Cantidad de bytes con valor 0

Porcentaje vacío: Relación nulobytes/tamaño total

Ediciones: Número de bytes modificados

Entropía: Nivel de aleatoriedad del archivo

⚙️ Configuración Técnica
Parámetros Ajustables
javascript
// Tamaño de página para carga progresiva
const PAGE_SIZE = 2048; // bytes por bloque

// Límites del panel lateral
min-width: 200px;
max-width: 800px;

// Modo de edición
realTimeEnabled: false; // LIVE: OFF por defecto
Navegación
Modo lectura: LIVE OFF → solo navegación con flechas

Modo edición: LIVE ON → navegación + edición directa

🐛 Solución de Problemas
Problema: No se puede editar
Solución: Activa ⚡ LIVE: ON en la barra superior

Problema: La imagen no se actualiza
Solución: Verifica que el archivo sea una imagen válida y que LIVE esté activo

Problema: Error al abrir archivo muy grande
Solución: El editor carga por bloques de 2KB. Archivos extremadamente grandes pueden ser lentos

📁 Estructura del Proyecto
text
matrix-binary-suite/
├── index.html          # Aplicación principal
├── README.md           # Documentación
└── LICENSE             # Licencia MIT
🧪 Requisitos del Sistema
Navegador: Chrome 80+, Firefox 75+, Edge 80+, Safari 13+

JavaScript: ES6+

Memoria: Recomendado 512MB RAM para archivos grandes

Sistema: Windows, macOS, Linux (cualquier SO con navegador)

📝 Ejemplos de Uso
Editar un Byte
text
1. Activar LIVE: ON
2. Hacer clic en un byte (ej: "4A")
3. Escribir "FF"
4. El cambio se guarda automáticamente
Buscar Texto
text
1. Búsqueda → Texto (Ignorar Mayúsculas)
2. Ingresar "HELLO"
3. Usar ◀ Ant. / Sig. ▶ para navegar resultados
Analizar Imagen BMP
text
1. Abrir archivo .bmp
2. Ver vista previa en panel izquierdo
3. Hacer clic en la imagen → salta al byte del píxel
4. Modificar bytes → la imagen se actualiza
🤝 Contribuciones
Las contribuciones son bienvenidas. Por favor:

Fork el proyecto

Crea una rama (git checkout -b feature/nueva-funcionalidad)

Commit tus cambios (git commit -m 'Agrega nueva funcionalidad')

Push a la rama (git push origin feature/nueva-funcionalidad)

Abre un Pull Request

📄 Licencia
MIT License - Libre para uso personal y comercial.

✨ Créditos
Desarrollado como herramienta profesional de análisis hexadecimal y forense digital.

Versión: 7.0
Última actualización: 2024
Estado: ✅ Estable

📞 Soporte
Para reportar problemas o sugerir mejoras:

Abrir un Issue en GitHub

Documentar el problema con pasos para reproducir

Adjuntar archivo de ejemplo si es posible

🔒 Notas de Seguridad
El editor trabaja completamente en local (client-side)

No se envían datos a ningún servidor

Los archivos permanecen en tu navegador

Ideal para análisis forense y edición segura

Matrix Binary Suite - Edición hexadecimal profesional, ahora en tu navegador.

text

Este README proporciona:

1. **Visión general clara** del propósito de la herramienta
2. **Instrucciones paso a paso** para instalación y uso
3. **Tablas de atajos de teclado** para referencia rápida
4. **Desglose de funcionalidades** con descripciones concisas
5. **Ejemplos prácticos** de casos de uso comunes
6. **Solución de problemas** para errores frecuentes
7. **Información técnica** para desarrolladores
8. **Estructura del proyecto** y requisitos del sistema























