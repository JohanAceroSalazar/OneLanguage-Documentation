# Permisos y capacidades

El proyecto declara `expo-camera`; `app.json` configura la descripción de cámara en iOS y `android.permission.CAMERA` en Android. La aplicación también maneja preferencias funcionales `camera` y `audio` por API, que complementan —sin sustituir— el permiso nativo de cámara. La lectura usa `expo-speech`; no se observó un permiso de audio de Android declarado. Los mensajes y comportamiento en dispositivos reales requieren validación en ejecución.
