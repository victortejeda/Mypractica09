# Proyecto de Audio - Android

## Descripción
Esta es una aplicación Android completa que demuestra el manejo de audio utilizando Jetpack Compose. La aplicación incluye:
- Reproducción de sonidos cortos con SoundPool
- Reproducción de canciones largas con MediaPlayer
- Grabación de audio con MediaRecorder
- Interfaz moderna con Jetpack Compose
- Navegación entre pantallas
- Manejo de permisos del sistema

## Características
- **Pantalla de Bienvenida**: Muestra información de los autores
- **Pantalla de Audio**: Controles para reproducir y grabar audio
- **Log en Tiempo Real**: Muestra todas las acciones realizadas
- **Manejo de Permisos**: Solicita permisos de grabación automáticamente
- **Guardado de Grabaciones**: Las grabaciones se guardan en la librería multimedia del dispositivo

## Configuración Requerida

### 1. Archivos de Audio
**IMPORTANTE**: Necesitas reemplazar los archivos de marcador de posición en `app/src/main/res/raw/` con archivos de audio reales:

- `tono_corto.mp3` - Sonido corto para el primer botón
- `otro_tono.mp3` - Sonido corto para el segundo botón  
- `cancion_larga.mp3` - Canción más larga para el tercer botón

**Restricciones de nombres**:
- Solo letras minúsculas, números y guión bajo (_)
- No usar guiones (-) ni espacios
- Formato recomendado: .mp3 o .ogg

### 2. Permisos
Los permisos ya están configurados en `AndroidManifest.xml`:
- `RECORD_AUDIO` - Para grabar audio
- `WRITE_EXTERNAL_STORAGE` - Para guardar archivos (Android < 29)
- `READ_EXTERNAL_STORAGE` - Para leer archivos (Android < 29)

### 3. Dependencias
Las dependencias necesarias ya están añadidas en `build.gradle.kts`:
- Navigation Compose
- Lifecycle ViewModel Compose

## Funcionalidades

### Botones de Sonido
- **Tono 1**: Reproduce el primer archivo de audio corto
- **Tono 2**: Reproduce el segundo archivo de audio corto

### Botón de Canción
- **Reproducir Canción**: Inicia la reproducción de la canción larga
- **Detener Canción**: Detiene la reproducción actual

### Botón de Grabación
- **Grabar Conversación**: Inicia la grabación de audio
- **Detener Grabación**: Detiene la grabación y la guarda

## Estructura del Código

### AudioViewModel
- Maneja toda la lógica de audio
- Gestiona estados de reproducción y grabación
- Controla SoundPool, MediaPlayer y MediaRecorder

### MainActivity
- Configura la aplicación y los permisos
- Inicializa el ViewModel
- Maneja la solicitud de permisos

### Pantallas
- `WelcomeScreen`: Pantalla de bienvenida con información de autores
- `AudioProjectScreen`: Pantalla principal con controles de audio

## Uso

1. **Compilar y Ejecutar**: Compila el proyecto en Android Studio
2. **Conceder Permisos**: La app solicitará permisos de grabación automáticamente
3. **Probar Sonidos**: Usa los botones de tono para probar archivos cortos
4. **Reproducir Canción**: Usa el botón de canción para archivos largos
5. **Grabar Audio**: Usa el botón de grabación para crear grabaciones

## Notas Importantes

- **Archivos de Audio**: Debes proporcionar tus propios archivos de audio
- **Permisos**: La app solicita permisos de grabación en tiempo de ejecución
- **Almacenamiento**: Las grabaciones se guardan en la carpeta "Music/Recordings/"
- **Compatibilidad**: Funciona en Android API 21+ (Android 5.0+)

## Autores
- Henry Castro (1-21-4112)
- Lissette Rodríguez (1-19-3824)  
- Miguel Berroa (2-16-3694)

## Tecnologías Utilizadas
- Kotlin
- Jetpack Compose
- Android Media APIs
- Navigation Compose
- ViewModel y StateFlow
- Coroutines
