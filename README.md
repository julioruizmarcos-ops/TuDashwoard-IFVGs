# Trading Journal PWA - TuDashboard IFVGs

## 📊 Descripción

Una **Progressive Web App (PWA)** profesional y completa para traders, enfocada en el análisis de operaciones con confluencias estratégicas algorítmicas. Diseñada para máxima precisión en métricas de Trading, análisis de Fair Value Gaps (FVGs), Draw on Liquidity (DOL), y correlaciones de activos.

## ✨ Características Principales

### 📈 Dashboard de Métricas en Tiempo Real
- **Total de Trades**: Contador automático de todas las operaciones
- **Ganadores/Perdedores**: Estadísticas segregadas
- **Breakeven (Trades 0)**: Identificación de operaciones neutras
- **Win Rate**: Porcentaje de victorias calculado automáticamente

### 📅 Calendario Operativo Visual
- Marcadores de color para cada trade (Ganador ✅ / Perdedor ❌ / Breakeven ⏸️)
- Navegación intuitiva por meses
- Vista de trades por fecha
- Información flotante al pasar el ratón

### 🎯 Registro de Operaciones Completo
- **Fecha**: Selección automática con valor por defecto (hoy)
- **Activo**: NQ (Nasdaq), ES (S&P 500), o Ambos
- **Resultado**: Ratio R:R obtenido (soporta decimales)
- **Confluencias**: 16 opciones categorizadas por tipo de análisis

### 🔧 Confluencias Estratégicas (16 tipos)

#### FVG / IFVG
- IFVG en FVG de 5m patrocinado por 15m
- IFVG en FVG de 5m patrocinado por 30m+
- BE en FVG 5m sin patrocinio

#### Continuación / DOL
- Continuación tras DOL en FVG 5m patrocinado por 15m
- Continuación tras DOL en FVG 5m patrocinado por 30m+
- Continuación una vez tomado el DOL en FVG de 15m

#### Análisis Algorítmico
- Manipulación real
- Sin manipulación real

#### Correlación de Activos
- Ambos activos en zona de reacción
- Solo NQ en zona de reacción
- Solo ES en zona de reacción

#### Divergencia SMT
- Solo NQ en zona de reacción + SMT
- Solo ES en zona de reacción + SMT

### 📋 Historial Técnico
- Tabla completa con historial ordenado (más reciente primero)
- Filtrado por confluencia
- Badges de estado (Ganador/Perdedor/Breakeven)
- Acciones: Editar y Eliminar operaciones
- Vista responsiva con scroll horizontal

### 💾 Almacenamiento Local
- Datos persistentes en **localStorage**
- No requiere servidor backend
- Funciona completamente offline

### 📲 PWA Instalable
- Instalable en iOS y Android
- Funciona sin conexión a internet
- Acceso rápido desde pantalla de inicio
- Soporte para iconos adaptables

## 🚀 Instalación

### Acceso Online
La app está publicada en GitHub Pages:
```
https://julioruizmarcos-ops.github.io/TuDashwoard-IFVGs
```

### Instalación Local
1. Clona el repositorio:
```bash
git clone https://github.com/julioruizmarcos-ops/TuDashwoard-IFVGs.git
cd TuDashwoard-IFVGs
```

2. Abre el archivo `index.html` en tu navegador

### Instalación como Aplicación (PWA)

#### En navegadores soportados:
- **Chrome/Edge**: Botón "📥 Instalar App" arriba a la derecha
- **iOS Safari**: Compartir → Añadir a pantalla de inicio
- **Android Chrome**: Menú → Instalar app

## 📱 Uso

### 1. Registrar una Operación
1. Completa la fecha (por defecto: hoy)
2. Selecciona el activo operado
3. Ingresa el resultado en R:R (ej: 2.5, -1, 0)
4. Marca las confluencias que se dieron
5. Click en "Guardar Operación"

### 2. Ver Estadísticas
- El dashboard se actualiza automáticamente
- Observa Win Rate, ganadores, perdedores

### 3. Consultar Calendario
- Navega por meses con los botones ← →
- Los puntos de colores indican trades del día
- Hover para ver detalles rápidos

### 4. Filtrar Historial
- Usa el select "Filtrar por Confluencia"
- Visualiza solo trades con una confluencia específica

### 5. Editar/Eliminar
- Click "Editar" para modificar un trade
- Click "Eliminar" para borrar (con confirmación)
- "Cancelar Edición" para salir de la edición

## 🛠️ Tecnologías

- **HTML5**: Estructura semántica
- **CSS (Tailwind CSS v4)**: Estilos CDN dinámicos
- **JavaScript Vanilla**: Lógica sin dependencias
- **Service Worker**: Capacidades offline
- **localStorage**: Persistencia de datos
- **Web App Manifest**: Instalabilidad PWA

## 📊 Estructura de Datos

Cada trade se almacena como:
```json
{
  "id": "t_1718016823910",
  "date": "2026-06-09",
  "asset": "NQ",
  "result": 2.5,
  "confluencias": ["ifvg_fvg_5m_sp_15m", "ambos_activos_zona_reaccion"]
}
```

## 🎨 Diseño

- **Tema Dark**: Optimizado para reducción de fatiga visual
- **Colores estratégicos**:
  - 🟢 Verde: Trades ganadores
  - 🔴 Rojo: Trades perdedores
  - 🔵 Azul: Breakevens
  - 🟣 Indigo: Interfaz principal
- **Responsivo**: Desde mobile hasta desktop
- **Accesibilidad**: Contraste de colores WCAG AA

## 🔒 Privacidad

- ✅ Todos los datos se guardan localmente en tu dispositivo
- ✅ No se envía información a servidores externos
- ✅ No hay tracking ni analytics
- ✅ Función offline completa

## 📈 Casos de Uso

- ✅ Day Traders en Futuros (ES, NQ)
- ✅ Swing Traders
- ✅ Análisis técnico con confluencias
- ✅ Backtesting y revisión de operaciones
- ✅ Seguimiento de patrones FVG/IFVG
- ✅ Análisis de manipulaciones algorítmicas

## 🐛 Reporte de Bugs

Si encuentras algún problema:
1. Abre una issue en GitHub
2. Describe el problema detalladamente
3. Incluye pasos para reproducir

## 📝 Notas Importantes

- El valor **0** en resultado se cuenta como **Breakeven** de forma estricta
- Los trades se muestran ordenados del más reciente al más antiguo
- Los datos se guardan automáticamente en localStorage
- La PWA funciona completamente offline tras la primera carga

## 🌐 Compatibilidad

| Navegador | Desktop | Mobile |
|-----------|---------|--------|
| Chrome    | ✅ Full | ✅ PWA |
| Firefox   | ✅ Full | ✅ Full |
| Safari    | ✅ Full | ✅ PWA |
| Edge      | ✅ Full | ✅ PWA |

## 📄 Licencia

MIT - Libre para uso personal y comercial

## 👤 Autor

**julioruizmarcos-ops** - Trading Journal PWA Developer

---

**¿Necesitas ayuda?** Revisa la documentación o abre un issue en el repositorio.
