# Controlador de Gastos Mensuales

Una aplicación web moderna para gestionar y controlar gastos mensuales con persistencia de datos en archivos Excel.

## Características

- ✨ **Interfaz moderna y responsiva** con diseño atractivo
- 📊 **Estadísticas en tiempo real** (total, gastos del mes, promedio)
- 📅 **Filtrado por mes** para ver gastos específicos
- 📈 **Resumen mensual** con totales por período
- 🗂️ **Categorización de gastos** (Alimentación, Transporte, etc.)
- 💾 **Persistencia de datos** en archivos Excel
- 🔄 **CRUD completo** (Crear, Leer, Actualizar, Eliminar)
- 📱 **Diseño responsive** para móviles y tablets

## Tecnologías Utilizadas

- **Backend**: Python + Flask
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Base de Datos**: Archivos Excel (.xlsx)
- **Librerías**: pandas, openpyxl

## Instalación

### Prerrequisitos

- Python 3.7 o superior
- pip (gestor de paquetes de Python)

### Pasos de Instalación

1. **Clonar o descargar el proyecto**
   ```bash
   git clone <url-del-repositorio>
   cd Controlador-de-Gastos
   ```

2. **Instalar dependencias**
   ```bash
   pip install -r requirements.txt
   ```

3. **Ejecutar la aplicación**
   ```bash
   python app.py
   ```

4. **Abrir en el navegador**
   ```
   http://localhost:5000
   ```

## Uso

### Agregar un Gasto

1. Haz clic en el botón **"Agregar Gasto"**
2. Completa el formulario:
   - **Fecha**: Selecciona la fecha del gasto
   - **Descripción**: Describe el gasto (ej: "Supermercado")
   - **Categoría**: Selecciona una categoría predefinida
   - **Monto**: Ingresa el valor del gasto
3. Haz clic en **"Guardar"**

### Editar un Gasto

1. En la tabla de gastos, haz clic en el ícono de **editar** (lápiz)
2. Modifica los campos necesarios
3. Haz clic en **"Guardar"**

### Eliminar un Gasto

1. En la tabla de gastos, haz clic en el ícono de **eliminar** (basura)
2. Confirma la eliminación

### Filtrar Gastos

- Usa el selector de **mes** para ver gastos de un período específico
- Selecciona **"Todos los meses"** para ver todos los gastos

### Ver Resumen Mensual

- Haz clic en **"Resumen Mensual"** para ver estadísticas por mes
- Se mostrarán los totales y cantidad de gastos por cada mes

## Estructura del Proyecto

```
Controlador-de-Gastos/
├── app.py                 # Aplicación principal Flask
├── requirements.txt       # Dependencias de Python
├── README.md             # Este archivo
├── templates/
│   └── index.html        # Página principal
└── data/
    └── gastos.xlsx       # Archivo Excel con los datos (se crea automáticamente)
```

## API Endpoints

- `GET /api/expenses` - Obtener todos los gastos
- `POST /api/expenses` - Crear nuevo gasto
- `PUT /api/expenses/<id>` - Actualizar gasto existente
- `DELETE /api/expenses/<id>` - Eliminar gasto
- `GET /api/expenses/monthly/<year>/<month>` - Obtener gastos por mes
- `GET /api/expenses/summary` - Obtener resumen mensual

## Categorías de Gastos

- **Alimentación**: Comida, supermercado, restaurantes
- **Transporte**: Gasolina, transporte público, mantenimiento
- **Entretenimiento**: Cine, salidas, hobbies
- **Salud**: Medicamentos, consultas médicas
- **Educación**: Cursos, libros, material escolar
- **Vivienda**: Alquiler, servicios, mantenimiento
- **Servicios**: Internet, electricidad, agua
- **Otros**: Gastos misceláneos

## Persistencia de Datos

Los datos se guardan automáticamente en el archivo `data/gastos.xlsx`. Este archivo:

- Se crea automáticamente al agregar el primer gasto
- Se actualiza cada vez que se modifica, agrega o elimina un gasto
- Persiste entre sesiones y reinicios de la aplicación
- Puede ser abierto con Excel, Google Sheets o cualquier aplicación compatible

## Características Técnicas

- **Persistencia**: Los datos se mantienen aunque se cierre el navegador o se reinicie la aplicación
- **Responsive**: Funciona perfectamente en dispositivos móviles y tablets
- **Real-time**: Las estadísticas se actualizan automáticamente
- **Validación**: Formularios con validación de datos
- **Feedback**: Mensajes de confirmación y error para el usuario

## Solución de Problemas

### Error al instalar dependencias
```bash
# Actualizar pip
python -m pip install --upgrade pip

# Instalar dependencias una por una
pip install Flask
pip install openpyxl
pip install pandas
```

### Error al ejecutar la aplicación
- Verificar que Python esté instalado correctamente
- Verificar que todas las dependencias estén instaladas
- Verificar que el puerto 5000 no esté en uso

### Los datos no se guardan
- Verificar que la carpeta `data` tenga permisos de escritura
- Verificar que no haya otro proceso usando el archivo Excel

## Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## Contacto

Si tienes preguntas o sugerencias, no dudes en contactar.

---

¡Disfruta gestionando tus gastos de manera eficiente! 💰
