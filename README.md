# caso_base

Una app pensada para estudiantes de Licenciatura en Ciencias de la Computación de la UNR que junta en un solo lugar lo que a cualquier ingresante le cuesta encontrar disperso: horarios, aulas, correlativas, porcentaje de avance de la carrera y estadísticas de tiempo de estudio dedicado a cada materia.

Nació en la **Hackaton JCC 2026**, organizada en el marco de las JCC XXIV por la Facultad de Ciencias Exactas, Ingeniería y Agrimensura de la UNR, en Rosario.

🔗 **App:** [hackaton-app-bay.vercel.app](https://hackaton-app-bay.vercel.app/)


## Funcionalidades

- **Selección de materias** por año y cuatrimestre, con los datos actualizados desde una API pública desarrollada para este evento en particular.
- **Árbol de correlativas** interactivo: marcás tu condición en cada materia (No cursable, Regular, Libre, Aprobada) y el árbol refleja automáticamente qué podés cursar.
- **Calendario** con vista de semana y mes, con las fechas de parciales marcadas.
- **Horario semanal** armado automáticamente a partir de las materias seleccionadas, con detección de superposiciones.
- **Estadísticas** de tiempo de estudio por materia y de forma global.
- **Timer tipo pomodoro** integrado para registrar sesiones de estudio.
- Persistencia en el navegador: los datos no se pierden al recargar la página.

## Stack

- [Vue 3](https://vuejs.org/) + `<script setup>`
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [Pinia](https://pinia.vuejs.org/) para el manejo de estado
- Desplegado en [Vercel](https://vercel.com/)
- Desarrollado con asistencia de [v0](https://v0.dev/)

Los datos de materias, horarios, correlativas y calendario académico se consumen en vivo desde la [API](https://fceia-api.ariloc.ar/docs), de solo lectura y sin autenticación.

## Desarrollo local

Cloná el repo e instalá las dependencias:

```bash
git clone https://github.com/ssalvatico/hackaton-app.git
cd hackaton-app
npm install
```

Creá un archivo `.env` en la raíz con la URL base de la API:

```bash
VITE_API_URL=https://fceia-api.ariloc.ar
```

Levantá el servidor de desarrollo:

```bash
npm run dev
```

Para generar el build de producción:

```bash
npm run build
```

## Equipo

- [Lucio Oviedo](https://github.com/Haiduz)
- [Santiago Salvático](https://github.com/ssalvatico)

## Agradecimientos

A la organización de las JCC XXIV por el espacio y la experiencia.
