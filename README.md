# UCV Medisalud

Este proyecto corresponde a la plataforma **UCV Medisalud**, una solución digital orientada a la gestión y atención médica, desarrollada para la Universidad César Vallejo. El sistema está compuesto por tres aplicaciones principales, cada una ubicada en su respectiva carpeta:

## Estructura del Proyecto

- **app-admin-medisalud/**: Aplicación para administradores del sistema. Permite la gestión de usuarios, médicos, pacientes, y la administración general de la plataforma.
- **app-user-medisalud/**: Aplicación para usuarios/pacientes. Permite la gestión de citas, visualización de historial médico y acceso a servicios de salud.
- **app-doctor-medisalud/**: Aplicación para médicos. Permite la gestión de pacientes, consultas, recetas y seguimiento clínico.

Cada aplicación está desarrollada con tecnologías modernas (Angular, Ionic, Capacitor) y cuenta con su propia configuración y dependencias.

## Instalación y uso

1. Clona este repositorio:
   ```bash
   git clone https://github.com/ucv-renacyt/ucv-medisalud.git
   ```
2. Ingresa a la carpeta de la aplicación que deseas ejecutar (por ejemplo, `app-admin-medisalud`).
3. Instala las dependencias:
   ```bash
   npm install
   ```
4. Ejecuta la aplicación:
   ```bash
   ionic serve
   ```

---

## Generar APK de prueba

Requisitos: Node.js, JDK 17 y Android SDK con la plataforma 34 y Build Tools 34.0.0.
Configura `JAVA_HOME` y `ANDROID_HOME` según las rutas de tu equipo.

Ejecuta estos comandos dentro de cada aplicación (`app-user-medisalud`,
`app-doctor-medisalud` y `app-admin-medisalud`):

```bash
npm ci
npm run build
npx cap sync android
cd android
sh ./gradlew assembleDebug
```

Cada APK se genera en `android/app/build/outputs/apk/debug/app-debug.apk`.
Son APK instalables firmados con la clave de depuración local; para publicar
en una tienda se necesita una compilación de distribución con su firma propia.
