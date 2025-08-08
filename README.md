# Scrapin-OCC

Un scraper web para extraer información de vacantes de OCC.com.mx usando Puppeteer.

## 🚀 Características

- **Scraping automático**: Extrae información completa de vacantes
- **Múltiples formatos**: Genera archivos JSON, CSV, Excel y PDF
- **Interfaz web**: Interfaz gráfica para realizar búsquedas
- **Navegación por páginas**: Recorre automáticamente todas las páginas de resultados

## 📁 Estructura del Proyecto

```
Scrapin-OCC/
├── scrape.js              # Script principal de scraping
├── web-interface/         # Interfaz web
│   ├── server.js          # Servidor Express
│   ├── index.html         # Página principal
│   ├── vacantes.html      # Página de resultados
│   └── package.json       # Dependencias de la interfaz
├── package.json           # Dependencias principales
└── vercel.json           # Configuración para Vercel
```

## 🛠️ Instalación

1. **Clona el repositorio**:
```bash
git clone https://github.com/tu-usuario/Scrapin-OCC.git
cd Scrapin-OCC
```

2. **Instala las dependencias**:
```bash
npm install
cd web-interface
npm install
cd ..
```

## 🎯 Uso

### Opción 1: Interfaz Web (Recomendado)

1. **Inicia el servidor**:
```bash
npm start
```

2. **Abre tu navegador** y ve a `http://localhost:3000`

3. **Ingresa un término de búsqueda** y haz clic en "Buscar"

4. **Visualiza los resultados** en la página de vacantes

### Opción 2: Línea de Comandos

```bash
node scrape.js
```

## 🌐 Despliegue en Vercel

**⚠️ Importante**: El scraping con Puppeteer **NO funciona** en Vercel debido a limitaciones del entorno serverless.

### Para desarrollo local:
- Usa `npm start` para ejecutar la interfaz web completa
- El scraping funcionará correctamente en tu máquina local

### Para Vercel:
- La interfaz web se mostrará correctamente
- El scraping mostrará un mensaje informativo
- Los archivos estáticos se servirán correctamente

## 📊 Archivos Generados

El scraper genera los siguientes archivos:

- `resultados.json` - Datos en formato JSON
- `resultados.csv` - Datos en formato CSV
- `resultados.xlsx` - Datos en formato Excel
- `resultados.pdf` - Datos en formato PDF

## 🔧 Configuración

### Variables de Entorno

Para la geocodificación, necesitas una API key de LocationIQ:

1. Ve a [LocationIQ](https://locationiq.com/)
2. Regístrate y obtén tu API key
3. Reemplaza la key en `web-interface/server.js`

## 🐛 Solución de Problemas

### Error 404 en Vercel
- Verifica que el archivo `vercel.json` esté en la raíz del proyecto
- Asegúrate de que las rutas estén configuradas correctamente

### Puppeteer no funciona
- En Vercel: Es normal, usa el proyecto localmente
- Localmente: Verifica que Chrome esté instalado

### Errores de scraping
- Verifica tu conexión a internet
- El sitio puede haber cambiado su estructura
- Intenta con diferentes términos de búsqueda

## 📝 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia MIT.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature
3. Commit tus cambios
4. Push a la rama
5. Abre un Pull Request

## 📞 Soporte

Si tienes problemas o preguntas:

1. Revisa la sección de problemas
2. Crea un nuevo issue
3. Incluye detalles sobre tu entorno y el error
