<div align="center">
  <h1> NOOR Calc - Calculadora 3D & Accesorios </h1>
  <p><i>Una solución móvil nativa, moderna y reactiva diseñada para la estimación precisa de costos de producción, inventario y precios de venta enfocada en <b>diseños y accesorios 3D</b>.</i></p>
  
  [![Kotlin](https://img.shields.io/badge/Kotlin-1.9%2B-7F52FF.svg?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
  [![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack_Compose-4285F4.svg?logo=android&logoColor=white)]()
  [![Architecture](https://img.shields.io/badge/Architecture-MVVM-003B57.svg)]()
  [![License](https://img.shields.io/badge/License-MIT-green.svg)]()
</div>

---

## Descripción General

**NOOR Calc** es una aplicación móvil nativa para Android desarrollada íntegramente en Kotlin. Diseñada bajo el patrón de arquitectura MVVM y utilizando interfaces declarativas, la aplicación centraliza y automatiza los cálculos de costos de manufactura especialmente para creadores de **diseños y accesorios 3D**.

El sistema permite a los emprendedores evitar pérdidas económicas mediante el cálculo granular de insumos, tiempo de máquina, mano de obra, gastos ocultos y márgenes de ganancia. Ofrece una experiencia de usuario (UX) sumamente fluida, soportada por flujos de estado reactivos que actualizan la facturación en tiempo real.

![App Preview](https://github.com/Lmendoza09/Calculadora-de-Precios-Noor/blob/main/NoorCalc.jpeg)

## Características Destacadas

### Motor de Cálculo para Impresión 3D (`NormalPrintScreen`)
- **Valoración por Calidad:** Cálculo dinámico basado en niveles de servicio (Estándar, Semi-Premium, Premium).
- **Análisis de Material:** Conversión automática del costo del filamento por kilo al peso específico en gramos de cada pieza.

### Módulo de Producción Mixta y Accesorios (`AccessoriesPrintScreen`)
- **Gestión Granular de Insumos:** Registro y cálculo fraccionado de materiales adicionales (cm de alambres y cadenas, unidades de piedras, aros, broches, resinas, etc.).
- **Costos de Modelado:** Integración del costo de la mano de obra del diseño digital directamente en la estructura de precios del producto físico.

### Gestión Financiera y Orquestación (`CalculadoraViewModel`)
- **Configuración Global Ajustable:** Panel de administración donde el usuario actualiza los precios unitarios de mercado de su materia prima, adaptándose a la inflación sin modificar código.
- **Protección de Rentabilidad:** Inclusión de variables porcentuales para *Gastos Ocultos* (desgaste de maquinaria, electricidad, mermas) y fijación de un *Margen de Ganancia* neto.
- **Cotización Editable:** Renderizado de una factura final interactiva que permite el sobre-escrito manual de subtotales antes de brindar el precio al cliente.

### Sistema de Historial y Recuperación (`SavedPrintsScreen`)
- **Gestión de Proyectos:** Guardado persistente de cotizaciones bajo nombres personalizados.
- **Búsqueda Indexada:** Filtrado reactivo en tiempo real para encontrar cálculos pasados y acelerar las respuestas a clientes recurrentes.

## Stack Tecnológico

| Componente | Tecnología | Propósito |
|------------|------------|-----------|
| **Core & Lógica** | `Kotlin` | Lenguaje de programación principal, moderno y seguro contra nulos (Null-Safety). |
| **Frontend UI** | `Jetpack Compose` | Construcción de interfaz gráfica declarativa, con animaciones fluidas y componentes de `Material Design 3`. |
| **Arquitectura** | `MVVM` | Separación estricta de las vistas y la lógica de negocio (Model-View-ViewModel). |
| **Reactividad** | `StateFlow` & `Coroutines` | Manejo asíncrono y transmisión de estados de la UI de manera unidireccional. |
| **Persistencia** | `SharedPreferences` | Almacenamiento local persistente para las configuraciones globales de precios e historial. |
| **Serialización** | `JSON` | Estructuración y parseo de los datos del historial de cotizaciones guardadas. |

## Arquitectura de Estado y Almacenamiento

Para garantizar una experiencia sin interrupciones y un rendimiento óptimo, el sistema emplea una estrategia moderna de gestión de datos:
- **Flujo de Datos Unidireccional (UDF):** La interfaz gráfica únicamente observa y reacciona al `StateFlow` inmutable emitido por el `ViewModel`. Todo evento del usuario se procesa centralizadamente, recalculando totales de forma instantánea.
- **Almacenamiento Local Desacoplado:** Las configuraciones críticas de mercado (precios base) y el historial se serializan y resguardan en el almacenamiento privado de la aplicación, garantizando que el usuario nunca pierda su estructura de costos al cerrar la aplicación.

## Link de Demostración

💾 [Video Demostración del Sistema](https://youtube.com/shorts/3aVReUWOCzA?feature=share)
