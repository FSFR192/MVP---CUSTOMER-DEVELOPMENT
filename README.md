FACEATTEND - Plataforma de Proctoreo con Tecnología MERNEsta es una aplicación Full Stack desarrollada con el stack MERN (MongoDB, Express, React, Node.js) diseñada para la supervisión de exámenes en línea.
1. Configuración de Variables de Entorno (.env)El proyecto requiere variables de entorno cruciales para la conexión a la base de datos y la autenticación. Debes crear un archivo llamado .env dentro de la carpeta backend y rellenarlo con tus valores.Creación del ArchivoNavega a la carpeta backend.Copia o renombra el archivo .env.example a .env.Rellena las variables con tus credenciales.Contenido del Archivo .env (Ejemplo)Fragmento de código# Node.js environment
NODE_ENV=development

# Puerto para el servidor backend
PORT=5000

# URL de conexión de MongoDB Atlas (¡CRUCIAL!)
# Asegúrate de codificar la contraseña si contiene caracteres especiales como '@' (%40).
MONGO_URL="mongodb+srv://fenandofloresrivera_db_user:tu_contraseña@faceattend.qxf2urh.mongodb.net/?appName=FACEATTEND"

# Clave secreta JWT para la autenticación
# Usa una cadena larga y segura.
JWT_SECRETO="TU_CLAVE_LARGA_SECRETA_AQUI"
2. Instalación de DependenciasEjecuta los siguientes comandos para asegurar que todas las librerías necesarias estén instaladas en las carpetas correctas.Instalar dependencias del Backend:Bashcd backend
npm install
Instalar dependencias del Frontend:Bashcd frontend
npm install
Regresar a la carpeta principal del Backend:Bashcd ..
3. Comandos de EjecuciónPara iniciar la aplicación, es fundamental usar el script que levanta el backend y el frontend de forma simultánea.Iniciar la Aplicación (Backend y Frontend a la vez)Ejecuta este comando desde la carpeta backend:Bashnpm run dev
ProcesoPuertoEstadoBackend (Node.js/Express)http://localhost:5000Debería mostrar MongoDB ConnectedFrontend (React)http://localhost:3000 (o 3001)Se abrirá la interfaz de usuario en el navegadorIniciar Solo el Backend (Para Debugging)Si necesitas verificar la conexión a MongoDB o probar solo la API. Ejecuta desde la carpeta backend:Bashnpm run server
