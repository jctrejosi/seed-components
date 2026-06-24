# seed-components

Biblioteca de componentes React construida con TypeScript y CSS Modules.

`seed-components` proporciona componentes reutilizables organizados por familias visuales (constellations), permitiendo mantener la misma funcionalidad con diferentes estilos visuales.

Diseñada para aplicaciones web, sistemas administrativos, landing pages, portafolios, agendas, formularios y paneles de gestión.

---

## características

- Componentes React escritos en TypeScript.
- Arquitectura basada en constellations (`Andromeda`, `Antlia`, etc.).
- CSS Modules para aislamiento de estilos.
- Personalización mediante CSS Variables.
- Compatible con React + Vite.
- Distribución optimizada para npm.
- Storybook para documentación visual.
- Sistema de traducciones integrado en múltiples componentes.
- Componentes desacoplados y reutilizables.

---

## instalación

```bash
npm install seed-components
```

o

```bash
yarn add seed-components
```

---

## uso básico

Importa cualquier componente:

```tsx
import { AlertAndromeda } from 'seed-components'

export default function App() {
  return (
    <AlertAndromeda
      title="Operación exitosa"
      message="Los datos fueron guardados correctamente"
      type="success"
    />
  )
}
```

---

## componentes disponibles

### alert

- AlertAndromeda

### appointment form

- AppointmentFormAndromeda

### calendar

- CalendarAndromeda
- CalendarAntlia

### contact form

- ContactFormAndromeda
- ContactFormAntlia

### file downloader

- FileDownloaderAndromeda

### y más...

La librería continúa creciendo mediante nuevas constellations y componentes reutilizables.

---

## filosofía de las constellations

Cada componente puede existir en múltiples variantes visuales.

Ejemplo:

```tsx
import {
  ContactFormAndromeda,
  ContactFormAntlia,
} from 'seed-components'
```

Ambos componentes resuelven el mismo problema, pero presentan interfaces y experiencias visuales distintas.

Esto permite mantener consistencia funcional mientras se adapta el diseño a diferentes proyectos.

---

## personalización mediante css variables

Los componentes utilizan variables CSS para facilitar la tematización.

Ejemplo:

```css
:root {
  --calendar-primary: #2563eb;
  --calendar-text: #111827;
  --calendar-bg: #ffffff;
}
```

Posteriormente los componentes consumirán estas variables automáticamente.

---

## estructura del proyecto

```text
.
├── bundle
│   ├── index.css
│   ├── index.es.js
│   └── index.umd.js
│
├── src
│   ├── components
│   │   ├── Alert
│   │   │   └── Andromeda
│   │   │
│   │   ├── AppointmentForm
│   │   │   └── Andromeda
│   │   │
│   │   ├── Calendar
│   │   │   ├── Andromeda
│   │   │   └── Antlia
│   │   │
│   │   ├── ContactForm
│   │   │   ├── Andromeda
│   │   │   └── Antlia
│   │   │
│   │   └── ...
│   │
│   ├── types
│   ├── utils
│   └── index.ts
│
├── .storybook
├── package.json
├── vite.config.ts
├── tsconfig.json
└── README.md
```

---

## desarrollo local

Instalar dependencias:

```bash
npm install
```

Ejecutar entorno de desarrollo:

```bash
npm run dev
```

Ejecutar Storybook:

```bash
npm run storybook
```

Construir librería:

```bash
npm run build
```

Generar bundle para publicación:

```bash
npm run bundle
```

---

## publicación en npm

Verifica el paquete:

```bash
npm run lint
npm run format
npm run bundle
```

Actualizar versión:

```bash
npm version patch
```

o

```bash
npm version minor
```

o

```bash
npm version major
```

Publicar:

```bash
npm publish --access public
```

---

## buenas prácticas

Antes de publicar:

```bash
npm run lint
npm run format
npm run build
npm run bundle
```

Verifica:

- Exportaciones del paquete.
- Tipos TypeScript generados.
- Bundle final.
- Storybook.
- Variables CSS documentadas.
- Compatibilidad en un proyecto externo.

Prueba local:

```bash
npm pack
```

Luego instala el `.tgz` generado en un proyecto consumidor.

---

## stack tecnológico

- React
- TypeScript
- Vite
- Storybook
- CSS Modules
- ESLint
- Prettier

---

## licencia

MIT