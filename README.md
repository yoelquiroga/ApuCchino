<p align="center">
  <img src="app/src/main/res/drawable/ic_letra_blanco.png" alt="ApuCchino Logo" width="200"/>
</p>

# ApuCchino

## 📋 Descripción
Aplicación Android para cafetería que permite explorar un catálogo de cafés, gestionar un carrito de compras y mantener una lista de favoritos, todo con persistencia local SQLite.

## ✨ Funcionalidades
- Catálogo de productos con filtrado por categorías (Espresso, Cappuccino, Latte, Americano)
- Autenticación local: registro e inicio de sesión de usuarios con validaciones
- Carrito de compras con control de cantidad, eliminación de ítems y cálculo de total
- Sistema de favoritos para marcar productos preferidos
- Vista detalle de producto con selector de cantidad y agregado al carrito
- Navegación inferior con cuatro secciones principales: Inicio, Carrito, Favoritos y Perfil
- Pantalla de perfil de usuario con datos personales y cierre de sesión
- Splash screen animado con onboarding inicial

## 🛠 Stack Tecnológico

<p align="center">
  <img src="https://img.shields.io/badge/Kotlin_2.0-DED0CE?style=flat-square&labelColor=DED0CE&logo=kotlin&logoColor=white" alt="Kotlin 2.0"/>
  <img src="https://img.shields.io/badge/Android_SDK_21--36-DED0CE?style=flat-square&labelColor=DED0CE&logo=android&logoColor=white" alt="Android SDK 21-36"/>
  <img src="https://img.shields.io/badge/SQLite-DED0CE?style=flat-square&labelColor=DED0CE&logo=sqlite&logoColor=white" alt="SQLite"/>
  <img src="https://img.shields.io/badge/Material_Design_3-DED0CE?style=flat-square&labelColor=DED0CE&logo=materialdesign&logoColor=white" alt="Material Design 3"/>
  <img src="https://img.shields.io/badge/RecyclerView-DED0CE?style=flat-square&labelColor=DED0CE" alt="RecyclerView"/>
  <img src="https://img.shields.io/badge/ConstraintLayout-DED0CE?style=flat-square&labelColor=DED0CE" alt="ConstraintLayout"/>
  <img src="https://img.shields.io/badge/Gradle_KTS_%2B_AGP_8.13-DED0CE?style=flat-square&labelColor=DED0CE&logo=gradle&logoColor=white" alt="Gradle KTS + AGP 8.13"/>
</p>

| Frontend | Backend / Persistencia | Build |
|---|---|---|
| XML Layouts, Material Design 3, RecyclerView, ConstraintLayout, BottomNavigationView | SQLite (SQLiteOpenHelper), SharedPreferences | Gradle (Kotlin DSL), AGP 8.13, Kotlin 2.0 |

## 📁 Estructura del Proyecto
```
app/
└── src/main/
    ├── java/com/example/proyectocafeteria/
    │   ├── adapter/              # RecyclerView adapters
    │   │   ├── CarritoAdapter.kt
    │   │   └── ProductoAdapter.kt
    │   ├── data/                 # Capa de datos
    │   │   └── AppDatabaseHelper.kt
    │   ├── entity/               # Modelos de datos
    │   │   ├── CarritoItem.kt
    │   │   ├── DetallePedido.kt
    │   │   ├── Pedido.kt
    │   │   ├── Producto.kt
    │   │   └── Usuario.kt
    │   └── ui/                   # Pantallas (Activities)
    │       ├── SplashActivity.kt
    │       ├── BienvenidaActivity.kt
    │       ├── AccesoActivity.kt
    │       ├── RegistrarseActivity.kt
    │       ├── HomeActivity.kt
    │       ├── DetalleProductoActivity.kt
    │       ├── CarritoActivity.kt
    │       ├── FavoritosActivity.kt
    │       └── PerfilActivity.kt
    ├── res/
    │   ├── layout/               # Layouts XML
    │   ├── drawable/             # Iconos, shapes y recursos gráficos
    │   ├── values/               # Strings, colores y temas
    │   ├── menu/                 # Menú de navegación inferior
    │   ├── anim/                 # Animaciones (splash)
    │   └── xml/                  # Reglas de backup y extracción
    └── AndroidManifest.xml
```

## 🚀 Requisitos Previos
- Android Studio Hedgehog (2024.x) o superior
- JDK 17
- Gradle 8.x (wrapper incluido en el proyecto)
- Dispositivo Android físico o emulador con API 21+

## 🔧 Configuración y Ejecución
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/apucchino.git
   ```

2. Abrir el proyecto en Android Studio:
   - `File` → `Open` → seleccionar la carpeta del proyecto

3. Sincronizar Gradle (las dependencias se descargan automáticamente):
   ```bash
   ./gradlew build
   ```

4. La base de datos SQLite local (`cafeteria.db`) se crea automáticamente al iniciar la app por primera vez, junto con una carga inicial de productos de ejemplo.

5. Ejecutar la aplicación:
   - Seleccionar un dispositivo Android (físico o emulador)
   - `Run ▶` o ejecutar:
   ```bash
   ./gradlew installDebug
   ```
